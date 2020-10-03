<template>
  <div>
    <v-container v-for="(item, i) in category" :key="i">
      <v-row>
        <div class="title py-4 px-2">
          {{ item.name }}
          <hr
            style="
              margin: 0px;
              background-color: #21252c;
              height: 2px;
              border: none;
            "
          />
        </div>
      </v-row>
      <v-row>
        <v-col
          v-for="(website_item, j) in item.website"
          :key="j"
          cols="12"
          sm="4"
          md="3"
          lg="2"
        >
          <v-card outlined :href="website_item.url" hover target="_blank">
            <v-container>
              <v-row justify="center" align="center" no-gutters>
                <v-col cols="2">
                  <v-img
                    class="nav-card mx-auto"
                    contain
                    eager
                    width="40"
                    height="40"
                    :src="website_item.logo"
                  ></v-img>
                </v-col>
                <v-col cols="10">
                  <v-card-title class="navigation_title pt-1 pb-0 subtitle-1"
                    >{{ website_item.name }}
                  </v-card-title>
                  <v-spacer />
                  <v-card-text
                    class="navigation_text pb-1 pt-0 body-4 font-weight-light"
                    >{{ website_item.introduction }}
                  </v-card-text>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    category: [
      {
        name: '资讯媒体',
        website: [
          {
            logo: '/image/logos/36kr.png',
            name: '36氪',
            introduction: '互联网+创业',
            url: 'https://www.36kr.com',
          },
          {
            logo: '/image/logos/huxiu.png',
            name: '虎嗅',
            introduction: '综合类高质量资讯',
            url: 'https://www.huxiu.com',
          },
          {
            logo: '/image/logos/ithome.png',
            name: 'IT之家',
            introduction: '互联网资讯社区',
            url: 'https://www.ithome.com',
          },
          {
            logo: '/image/logos/sspai.png',
            name: '少数派',
            introduction: '互联网+数码',
            url: 'https://sspai.com',
          },
        ],
      },
      {
        name: '设计采集',
        website: [
          {
            logo: '/image/logos/zcool.png',
            name: '站酷网',
            introduction: '设计师交流社区',
            url: 'https://www.zcool.com.cn',
          },
          {
            logo: '/image/logos/huaban.png',
            name: '花瓣网',
            introduction: '设计类交流社区，采集灵感',
            url: 'https://www.huaban.com',
          },
          {
            logo: '/image/logos/iconfont.png',
            name: '阿里巴巴图标库',
            introduction: '综合类高质量资讯',
            url: 'https://www.iconfont.cn',
          },
          {
            logo: '/image/logos/unsplash.png',
            name: 'UNSPLASH',
            introduction: '国外无版权摄影网站',
            url: 'https://www.unsplash.com',
          },
          {
            logo: '/image/logos/qiantu.png',
            name: '千图网',
            introduction: '要版权的，要钱的',
            url: 'https://www.58pic.com',
          },
          {
            logo: '/image/logos/qianku.png',
            name: '千库网',
            introduction: '隔壁的哥们',
            url: 'https://588ku.com',
          },
          {
            logo: '/image/logos/uicn.png',
            name: 'UI中国',
            introduction: 'UI类网站',
            url: 'https://www.ui.cn',
          },
          {
            logo: '/image/logos/wotu.png',
            name: '我图网',
            introduction: '免费（假）素材网站',
            url: 'https://www.ooopic.com',
          },
          {
            logo: '/image/logos/cnd.png',
            name: 'CND设计网',
            introduction: '设计师交流网站',
            url: 'https://www.ooopic.com',
          },
          {
            logo: '/image/logos/GoogleDesign.png',
            name: '谷歌设计官网',
            introduction: '谷歌设计语言，域名挺特别',
            url: 'https://design.google',
          },
          {
            logo: '/image/logos/pinterest.png',
            name: 'Pinterest',
            introduction: '国外老字号，偷素材专用',
            url: 'https://www.pinterest.com',
          },
          {
            logo: '/image/logos/doyoudo.png',
            name: 'DoYouDo',
            introduction: '小白老师笑声真好看',
            url: 'https://www.doyoudo.com',
          },
        ],
      },
      {
        name: '字体设计',
        website: [
          {
            logo: '/image/logos/ziticq.png',
            name: '字体传奇',
            introduction: '字体品牌设计师交流网站',
            url: 'http://www.ziticq.com/',
          },
          {
            logo: '/image/logos/hellofont.png',
            name: '字由网站',
            introduction: '设计师必备利器',
            url: 'https://www.hellofont.cn',
          },
          {
            logo: '/image/logos/source-han-serif.png',
            name: '思源宋体官网',
            introduction: '思源宋体，懂的都懂',
            url: 'https://source.typekit.com',
          },
          {
            logo: '/image/logos/Fondertype.png',
            name: '方正字体库',
            introduction: '老字号了',
            url: 'https://www.foundertype.com/',
          },
        ],
      },
      {
        name: '编程',
        website: [
          {
            logo: '/image/logos/easyicon.png',
            name: 'VisualGo',
            introduction: '算法可视化网站，因吹斯听',
            url: 'https://visualgo.net/',
          },
          {
            logo: '/image/logos/leetcode.png',
            name: 'LeetCode中国',
            introduction: '大神随意',
            url: 'https://leetcode-cn.com',
          },
          {
            logo: '/image/logos/stackoverflow.jpg',
            name: 'stackoverflow',
            introduction: '爆栈了，程序员问题交流',
            url: 'https://stackoverflow.com',
          },
          {
            logo: '/image/logos/v2ex.png',
            name: 'v2ex',
            introduction: 'v2ex，程序员上班摸鱼',
            url: 'https://www.v2ex.com',
          },
          {
            logo: '/image/logos/python123.png',
            name: 'Python123',
            introduction: '北理Python入门，能长头发',
            url: 'https://www.python123.io/',
          },
          {
            logo: '/image/logos/qianku.png',
            name: '千库网',
            introduction: '隔壁的哥们',
            url: 'https://588ku.com',
          },
        ],
      },
      {
        name: '娱乐吹水视频',
        website: [
          {
            logo: '/image/logos/youtube.png',
            name: 'YouTube',
            introduction: '第一摸鱼视频网站',
            url: 'https://www.youtube.com',
          },
          {
            logo: '/image/logos/vimeo.jpg',
            name: 'Vimeo',
            introduction: '高质量精品，强力推荐',
            url: 'https://www.vimeo.com',
          },
          {
            logo: '/image/logos/vmovier.png',
            name: 'V电影',
            introduction: '国内精品短视频',
            url: 'https://www.vmovier.com/',
          },
        ],
      },
      {
        name: '订阅类',
        website: [
          {
            logo: '/image/logos/NeteaseCloudMusic.png',
            name: '网易云第三方接口',
            introduction: '生不出人，我很抱歉',
            url: 'https://binaryify.github.io/NeteaseCloudMusicApi',
          },
          {
            logo: '/image/logos/HelloGithub.png',
            name: 'HelloGithub',
            introduction: '每周项目推荐，摸鱼必备',
            url: 'https://hellogithub.com/',
          },
        ],
      },
    ],
  }),
}
</script>

<style scoped>
.navigation_title {
  display: block;
  word-break: keep-all;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.navigation_text {
  display: block;
  word-break: keep-all;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
