
<script>
export default {
  // 1.简单的渲染一个元素
  // render: function(createElement) {
  //   return createElement("div", {
  //     class: {
  //       child: true,
  //       more: false
  //     },
  //     attrs: {
  //       id: "foo",
  //       name: "child"
  //     },
  //     style: {
  //       width: "100%",
  //       heigth: "50px"
  //     },
  //     domProps: {
  //       innerHTML: "child-innerHTML"
  //     }
  //   });
  // }
  // 2.添加子标签
  // render: function(createElement) {
  //   return createElement(
  //     "div",
  //     {
  //       class: {
  //         child: true,
  //         more: false
  //       }
  //     },
  //     [
  //       createElement("h1", "标题"),
  //       createElement("h2", {
  //         attrs: {
  //           id: "child-h1"
  //         },
  //         class: "more",
  //         style: {
  //           width: "100%",
  //           height: "50px"
  //         },
  //         domProps: {
  //           innerHTML: "h2"
  //         }
  //       })
  //     ]
  //   );
  // }
  // 3.this.$slots的用法
  // render: function(createElement) {
  //   let childheader = this.$slots.childheader,
  //     childbody = this.$slots.childbody,
  //     childfooter = this.$slots.childfooter;
  //   return createElement(
  //     "div",
  //     {
  //       class: "child",
  //       style: {
  //         width: "100%"
  //       }
  //     },
  //     [
  //       createElement("div", childheader),
  //       createElement("div", childbody),
  //       createElement("div", childfooter)
  //     ]
  //   );
  // }
  // 4.v-model
  // render: function(createElement) {
  //   let self = this;
  //   return createElement("div", [
  //     createElement("div", self.childinput),
  //     createElement("input", {
  //       domProps: {
  //         value: self.childinput
  //       },
  //       on: {
  //         input: function(event) {
  //           self.childinput = event.target.value;
  //         }
  //       }
  //     })
  //   ]);
  // },
  // data() {
  //   return {
  //     childinput: "childinput"
  //   };
  // },
  // watch: {
  //   childinput(v) {
  //     console.log(v);
  //   }
  // }
  //5. 作用域插槽
  // render: function(createElement) {
  //   let self = this;
  //   return createElement(
  //     "div",
  //     {
  //       style: {
  //         width: "100%",
  //         height: "50px"
  //       },
  //       class: "child"
  //     },
  //     [
  //       self.$scopedSlots.default({
  //         text: this.childmsg
  //       })
  //     ]
  //   );
  // },
  // data() {
  //   return {
  //     childmsg: "childmsg"
  //   };
  // }
  //
  // render: function(createElement) {
  //   return createElement("h1");
  // }
};
</script>

<style  scoped>
.child {
  background: pink;
}
.more {
  background: red;
}
</style>