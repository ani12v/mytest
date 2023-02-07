<template>
 <div>
    <el-tabs :key="category.name"
                      v-for="category in categorys"
                      
                      :name="category.name">
        <el-tab-pane  
                      >
          <!-- 本标签下文章内容 -->
          <el-row class="cardmain">
          <el-col class="card" :span="8"  v-for="h1 in category.cards1">
            <el-card style="margin: 0;padding: 0;">
              <!-- <div class="cardheader"> -->
                <div v-for="h2 in category.cards2">
                  {{h1.h1}}
                  <div v-for="h2 in category.cards2">
                    {{h2.h2}}
                    
                  </div>
                </div>
                <!-- <el-divider direction="vertical"></el-divider>
                <span>{{card.date}}</span>
                <el-divider direction="vertical"></el-divider>
                <span>{{card.tag}}</span> -->
              <!-- </div> -->
              <!-- <div style="display: flex; justify-content: center;">
                <div class="article">
                  <div class="gist1">{{card.title}}</div>
                  <div class="gist2">{{card.gist}}</div>
                </div>
              </div> -->
            </el-card>
          </el-col>
        </el-row>
        </el-tab-pane>
      </el-tabs>
 </div>
</template>
<script>
 export default {
  name:'Main',
   data () {
     return {
      activeName: '1',
      categorys:[
        {label:'推荐',cards:[
                              {username:"青训营官方账号",
                              date:"4月前",
                              tag:"青训营",
                              title:"叮咚！青训营-快乐出发Flag打卡活动来啦",
                              gist:"的数量开服就亏了多少解放路水电费水电费塞德里克封建时代双方都没法看了时代峰峻",
                              },
                              {username:"测试1",
                              date:"1.29",
                              tag:"马一珂",
                              title:"这是进行for循环嵌套测试",
                              gist:"这是第一页推荐",
                              }
                            ],
        },
      {cards1:[
          {h1:"青训营官方账号1",
          cards2:[{h2:"青训营官方账号2",
            cards3:[{h3:"青训营官方账号3",
              cards4:[{h4:"青训营官方账号4",
                cards5:[{h5:"青训营官方账号5",
                  cards6:[{h6:"青训营官方账号6",
                  },
            ],
                },
          ],
              },
        ],
            },
        ],

            },
        ],
          },
        ],
    },

    ]
     }
   },
   methods: {
    handleClick(tab, event) {
        console.log(tab, event);
    }
  }
 }
</script>
<style>
.cardmain{
  width: 100%;
  height: 100%;
}
.card{
  width: 100%;
  height: auto;
  padding-bottom: 1vw;
}
.cardheader{
  margin-left: 1vw;
  align-items: center;
  font-size: 13px;
  line-height: 22px;
  color: #4e5969;
}
.article{
   width: 80%;
   margin-left: 1vw;
   /* 超出的文本隐藏 */
  overflow:hidden;
  /* 溢出用省略号显示 */
  text-overflow:ellipsis;
  /* 溢出不换行  */
  white-space:nowrap;
}
.gist1{
  font-weight: 700;
  font-size: 2vw;
  line-height: 3vw;
  color: #1d2129;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  }
.gist2{
  line-height: 3vw;
  font-size: 1vw;
  color: #999;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  }
.img{
  width: 120px;
  height: 80px;
  margin-left: 1vw;
}

</style>
