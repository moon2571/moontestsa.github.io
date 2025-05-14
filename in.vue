<template>
  <div id="app">
    <!-- 头部区域，包含导航栏 -->
    <header>
      <nav>
        <ul>
          <li><router-link to="/about">关于我们</router-link></li>
          <li><router-link to="/services">服务</router-link></li>
          <li><router-link to="/contact">联系我们</router-link></li>
        </ul>
      </nav>
    </header>

    <!-- 关于我们部分 -->
    <section id="about">
      <div class="container">
        <!-- 公司介绍 -->
        <div class="about-intro">
          <p>{{ companyIntroduction }}</p>
        </div>
        <!-- 欢迎信息 和 留言链接 -->
        <div class="info-links">
          <div class="leave-message">
            <navigator url="/pages/index/index" class="fs36 mc">欢迎</navigator>
          </div>
          <div class="leave-message">
            <navigator url="/pages/index/liyan" class="fs36 mc">留言</navigator>
          </div>
          <!-- 显示所有留言的按钮 -->

        </div>
      </div>
      <!-- 留言窗口 -->

    </section>

    <!-- 服务部分 -->
    <section id="services">
      <h2>服务</h2>
      <p>我们提供以下服务：</p>
      <ul>
        <li>服务一</li>
        <li>服务二</li>
        <li>服务三</li>
      </ul>
    </section>

    <!-- 联系我们部分 -->
    <section id="contact">
      <div class="contact-header">
        <hr>
        <h2>联系我们</h2>
      </div>
      <p>你可以通过以下方式联系我们：</p>
      <p>Email: example@example.com</p>
    </section>

    <!-- 返回首页按钮 -->


    <!-- 底部区域 -->
    <footer>
      <p>© 2023 我的主页. 保留所有权利。</p> <!-- 版权信息 -->
    </footer>
  </div>
</template>

<script>

</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    /* 设置全局字体 */
    color: #2c3e50;
    /* 全局文字颜色 */
    margin-top: 60px;
    /* 顶部外边距 */
    text-align: center;
    /* 全局文本居中 */
  }

  header {
    background: #35495e;
    /* 头部背景颜色 */
    color: white;
    /* 头部文字颜色 */
    padding: 20px;
    /* 头部内边距 */
  }






  #about {
    margin-bottom: 20px;
    /* 为“关于我们”部分添加底部外边距 */
  }

  .container {
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    width: 80%;
  }

  .about-intro {
    width: 50%;
    text-align: left;
  }

  .info-links {
    width: 45%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }


  .leave-message {
    display: flex;
    margin-bottom: 10px;
    align-items: center;
    justify-content: center;
  }

  .fs36 {
    font-size: 36px;
    /* 设置字体大小为36px */
  }

  .message-window {
    border: 1px solid #ccc;
    /* 边框样式 */
    padding: 10px;
    /* 内边距 */
    margin: 20px auto;
    /* 外边距 */
    width: 80%;
    /* 宽度占容器的80% */
    max-height: 200px;
    /* 最大高度 */
    overflow-y: auto;
    /* 超出内容时显示垂直滚动条 */
    background-color: #f9f9f9;
    /* 背景颜色 */
    text-align: left;
  }

  #contact {
    margin-bottom: 20px;
    /* 为“联系我们”部分添加底部外边距 */
  }

  .contact-header {
    text-align: center;
    margin-bottom: 10px;
  }

  hr {
    border: 0;
    border-top: 1px solid #ccc;
    width: 80%;
    margin: 0 auto;
  }

  footer {
    background: #35495e;
    /* 底部背景颜色 */
    color: white;
    /* 底部文字颜色 */
    position: fixed;
    /* 固定底部位置 */
    bottom: 0;
    /* 底部距离视口底部为0 */
    width: 100%;
    /* 底部宽度占满整个视口 */
    padding: 10px 0;
    /* 底部内边距 */
    text-align: center;
  }

  @media (max-width: 600px) {
    .container {
      flex-direction: column;
      align-items: flex-start;
    }

    .info-links {
      width: 100%;
      align-items: center;
    }

    .about-intro {
      width: 100%;
    }

    .message-window {
      width: 90%;
      /* 小屏幕时宽度占容器的90% */
    }

    #contact {
      margin-top: 20px;
      /* 为“联系我们”部分添加顶部外边距 */
    }

    .contact-header hr {
      width: 90%;
    }
  }
</style>