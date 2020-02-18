<template>
  <div id="app" class="container">
    <div class="row">
      <div class="col-lg-6">
        <HelloWorld msg="Welcome to Your Vue.js Lifecycle" />
        <img alt="Vue logo" class="img-fluid" src="./assets/vue-life-cycle.png" />
        <h2>Link Tham Khảo: </h2>
         <ul>
          <li><a href="https://itzone.com.vn/vi/article/tim-hieu-ve-lifecycle-hooks-trong-vuejs/">https://itzone.com.vn/</a></li>
         <li><a href="https://viblo.asia/s/hoc-vuejs-va-laravel-tu-can-ban-den-nang-cao-z45bxjq6ZxY">https://viblo.asia/</a></li>
         <li><a href="https://toidicode.com/instance-trong-vue-js-317.html">https://toidicode.com</a></li>
         </ul>
      </div>
      <div class="col-lg-6 float-left">
        <h2>2.1 BeforeCreate</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi đồng bộ ngay sau khi instance được khởi tạo, trước khi quan sát dữ liệu và thiết lập event/watcher</li>
        </ul>
        <h2>2.2 Created</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi đồng bộ sau khi instance được tạo. Ở giai đoạn này, instance đã xử lý xong các tùy chọn có nghĩa là các thiết lập sau đã được thiết lập: quan sát dữ liệu, thuộc tính được tính toán (computed), phương thức (method), event/watcher callback. Tuy nhiên, giai đoạn mounting chưa được bắt đầu và thuộc tính $el sẽ không có sẵn.</li>
        </ul>
        <h2>2.3 BeforeMount</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi ngay trước khi quá trình mounting bắt đầu: function render được gọi lần đầu tiên và không được gọi trong quá trình render bên phía server</li>
        </ul>
        <h2>2.4 Mounted</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi sau khi instance đã được mounted, trong đó $el được thay thế bằng vm.$el mới được tạo. Nếu phiên bản gốc được gắn vào một phần tử trong tài liệu, vm.$el cũng sẽ ở trong tài liệu khi được gắn kết được gọi</li>
          <li>Lưu ý rằng mounted không đảm bảo rằng tất cả các thành phần con cũng đã được mounted. Nếu bạn muốn đợi cho đến khi toàn bộ view được hiển thị, bạn có thể sử dụng vm.$nextTick bên trong mounted</li>
          <li>Nó không được gọi trong quá trình render bên phía server</li>
        </ul>

        <h2>2.5 BeforeUpdate</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi khi dữ liệu thay đổi, trước khi DOM được cập nhật. Đây là một nơi tốt để truy cập DOM cũ trước nó được cập nhật, ví dụ: để loại bỏ listeners được thêm thủ công</li>
          <li>Nó không được gọi trong quá trình render bên phía server</li>
        </ul>
        <h2>2.6 Updated</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi sau khi thay đổi dữ liệu khiến DOM ảo được render lại và update.</li>
          <li>Thành phần của DOM sẽ được cập nhật khi hook này được gọi, vì vậy bạn có thể thực hiện các hoạt động phụ thuộc DOM tại đây. Tuy nhiên, trong hầu hết các trường hợp, bạn nên tránh thay đổi trạng thái bên trong hooks này.</li>
          <li>Để phản ứng với những thay đổi trạng thái, thay vào đó, sử dụng một tài sản hoặc người theo dõi được tính toán tốt hơn.</li>
          <li>Lưu ý rằng updated không đảm bảo rằng tất cả các thành phần con cũng đã được re-render. Nếu bạn muốn đợi cho đến khi toàn bộ chế độ xem được re-render, bạn có thể sử dụng vm.$nextTick bên trong updated :</li>
          <li>Nó không được gọi trong quá trình render bên phía server</li>
        </ul>

        <h2>2.7 Activated</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi khi một thành kept-alive được kích hoạt.</li>
          <li>Nó không được gọi trong quá trình render bên phía server</li>
        </ul>
        <h2>2.8 Deactivated</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi khi một thành kept-alive ngừng hoạt động.</li>
          <li>Nó không được gọi trong quá trình render bên phía serve</li>
        </ul>
        <h2>2.9 BeforeDestroy</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi ngay trước khi một instance Vue bị phá hủy. Ở giai đoạn này, instance vẫn đầy đủ chức năng.</li>
          <li>Nó không được gọi trong quá trình render bên phía serve</li>
        </ul>
        <h2>2.10 Destroyed</h2>
        <ul>
          <li>Kiểu: Function</li>
          <li>Mô tả: Được gọi sau khi một instance Vue đã bị phá hủy. Khi hook này được gọi, tất cả các lệnh của instance Vue bị mất ràng buộc, tất cả các trình lắng nghe sự kiện đã bị xóa và tất cả các instance Vue con cũng đã bị hủy</li>
          <li>Nó không được gọi trong quá trình render bên phía serve</li>
        </ul>

      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
