<template>
  <div class="home">
    <Banner class="mat"/>
    <Ad class="mat"/>
    <Member class="mat"/>
    <Info class="mat"/>
    <Type class="mat"/>
    <Details class="mat"/>
    <PhotoAlbum class="mat"/>
    <Surrounding class="mat"/>
  </div>
</template>

<script>
import Banner from "../components/Banner";
import Ad from "./home/Ad";
import Member from "./home/Member";
import Info from "./home/Info";
import Type from "./home/Type";
import Details from "./home/Details";
import PhotoAlbum from "./home/PhotoAlbum";
import Surrounding from "./home/Surrounding";

export default {
  components: {
    Banner,
    Ad,
    Member,
    Info,
    Type,
    Details,
    PhotoAlbum,
    Surrounding
  }
};
</script>

<style lang="less" scoped>
.home{
  width: 1280px;
  margin: 0 auto;
}

.mat{
  margin-top: 20px;
}
</style>