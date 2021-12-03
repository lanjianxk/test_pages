<template>
  <el-row :gutter="10">
    <el-col :span="24">
      <div class="logo-div">logo</div>
    </el-col>
    <el-col :span="24">
      <div class="margin">
        <el-carousel :interval="4000">
          <el-carousel-item v-for="(item, index) in bannerList" :key="index">
            <img
              src="../../common/images/avator.png"
              alt=""
              width="100%"
              height="100%"
            />
          </el-carousel-item>
        </el-carousel>
      </div>
    </el-col>
    <el-col :span="24">
      <div class="margin">
        <el-alert
          title="查询产品真伪"
          type="info"
          show-icon
          center
          :closable="false"
        >
        </el-alert>
        <el-button type="info" round style="width: 100%; margin-top: 20px"
          >查询官方认证机构</el-button
        >
      </div>
    </el-col>
    <el-col :span="24">
      <div class="margin">
        <el-form
          ref="form"
          :model="form"
          label-position="top"
          label-width="80px"
        >
          <el-form-item label="产品">
            <el-select
              v-model="form.projectName"
              placeholder="请选择产品！"
              style="width: 100%"
            >
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
          </el-form-item>
          <el-form-item label="地区">
            <el-select
              v-model="form.area"
              placeholder="请选择地区！"
              style="width: 100%"
            >
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
          </el-form-item>
          <el-form-item label="医院">
            <el-input
              v-model="form.hosName"
              placeholder="请输入医院名称！"
              style="width: 100%"
            ></el-input>
          </el-form-item>
          <el-form-item>
            <el-button type="info" round @click="onSubmit" style="width: 100%"
              >查询</el-button
            >
          </el-form-item>
        </el-form>
      </div>
    </el-col>
  </el-row>
</template>

<script>
import DataInfo from "@/data";
export default {
  name: "about",
  data() {
    return {
      bannerList: [
        {
          src: "",
        },
        {
          src: "",
        },
        {
          src: "",
        },
      ],
      form: {
        projectName: "",
        area: "",
        hosName: "",
      },
    };
  },
  methods: {
    onSubmit() {},
  },
};
</script>

<style scoped>
.carousel-div {
  padding: 0 4%;
}
.el-carousel__item:nth-child(2n) {
  background-color: rgb(179, 216, 255);
}
.el-carousel__item:nth-child(2n + 1) {
  background-color: rgb(217, 236, 255);
}
</style>

