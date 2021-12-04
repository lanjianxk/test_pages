<template>
  <div>
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
                <el-option label="区域1" value="shanghai"></el-option>
                <el-option label="区域2" value="beijing"></el-option>
                <el-option label="区域3" value="shanghai"></el-option>
                <el-option label="区域4" value="beijing"></el-option>
                <el-option label="区域5" value="shanghai"></el-option>
                <el-option label="区域6" value="beijing"></el-option>
                <el-option label="区域7" value="shanghai"></el-option>
                <el-option label="区域8" value="beijing"></el-option>
                <el-option label="区域9" value="shanghai"></el-option>
                <el-option label="区域10" value="beijing"></el-option>
                <el-option label="区域11" value="shanghai"></el-option>
                <el-option label="区域12" value="beijing"></el-option>
                <el-option label="区域13" value="shanghai"></el-option>
                <el-option label="区域14" value="beijing"></el-option>
                <el-option label="区域15" value="shanghai"></el-option>
                <el-option label="区域16" value="beijing"></el-option>
                <el-option label="区域17" value="shanghai"></el-option>
                <el-option label="区域18" value="beijing"></el-option>
                <el-option label="区域19" value="shanghai"></el-option>
                <el-option label="区域20" value="beijing"></el-option>
                <el-option label="区域21" value="shanghai"></el-option>
                <el-option label="区域22" value="beijing"></el-option>
                <el-option label="区域23" value="shanghai"></el-option>
                <el-option label="区域24" value="beijing"></el-option>
                <el-option label="区域25" value="shanghai"></el-option>
                <el-option label="区域26" value="beijing"></el-option>
                <el-option label="区域27" value="shanghai"></el-option>
                <el-option label="区域28" value="beijing"></el-option>
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
    <el-dialog
      title="医院信息"
      top="50px"
      width="90%"
      :visible.sync="dialogVisible"
      destroy-on-close
    >
      <el-descriptions direction="vertical" :column="1">
        <el-descriptions-item label="医院名称"
          >XXXXX医院名称</el-descriptions-item
        >
        <el-descriptions-item label="联系电话"
          >18100000000</el-descriptions-item
        >
        <el-descriptions-item label="地址"
          >XXXXXXXXXXXXXXX</el-descriptions-item
        >
      </el-descriptions>
    </el-dialog>
  </div>
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
      dialogVisible: false,
    };
  },
  methods: {
    onSubmit() {
      this.dialogVisible = true;
    },
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

