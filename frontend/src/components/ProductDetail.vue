<template>
  <div class="ProductDetail">
    <div class="container" id="home-box">
      <h1>{{ msg }}</h1>
      <div class="columns">
        <div class="column is-one-fifth">
            <img src="./../assets/item1.png" alt="Placeholder image">
            item1
        </div>
        <div class="column">
            <div class="card">
                <div class="card-header">
                    ITEM1
                </div>
                <div class="card-content">
                    kgkdfghdfjghdglghdfd;gjsg
                </div>
                <div class="card-footer">
                    <router-link to="/Home"><div class="button">Back</div></router-link>
                    <router-link to="/ProductDetail"><div class="button" disabled>Buy now</div></router-link>
                </div>
            </div>
          </div>
      </div>
    </div>
    <div class="navbar is-fixed-bottom" id="nav-bot">
        <div class="container" id="nav-bot-box">
            เพิ่มเครดิต
            <div class="button" @click="showLoginModal=true" id="button">เพิ่มเครดิต</div>
            <div class="button" @click="showLoginModal=true" id="button2">เพิ่มที่อยู่</div>
        </div>
    </div>
      <!-- popup Cradit -->
    
      <div class="modal-card" id="popUpCradit">
          <div class="container" >
              <div class="modal" id="page-modal">
                  <div class="modal-background"></div>
                  <section class="modal-card-body">
                      <div class="modal-content" id="screen">
                          <header id ="head" class="modal-card-head">
                              <p class="modal-card-title" style="text-align: center;">ใส่บัตรเครดิต/เดบิต</p>
                                  <button class="delete"  aria-label="close"></button>
                          </header>
                        <div class="columns is-multiline" style=" display: flex;" id="bodyPopUp">
                            <div class="field is-grouped" id="number">
                                <label  id="text" class="label">หมายเลขบัตร</label>
                                <label> <img src="../assets/visa.svg" width="20" height="10" style="  margin-left: 10px;"></label>
                                <label> <img src="../assets/mastercard.svg" width="20" height="10" style="  margin-left: 10px;"></label>
                            </div>
                            <div class="control">
                                <input class="input" type="text" placeholder="Ex. 1234567890123456">
                            </div>
                            <div class="field" id="name" style=" margin-top: 13px;">
                                <label class="label" id="text">ชื่อที่ปรากฏบนบัตร</label>
                                    <div class="control">
                                        <input class="input" type="text" placeholder="Ex. โสภณ จำปาซ่อนกลิ่น">
                                    </div>
                            </div>
                            <div class="field" id="province">
                                <label id="text" class="label">จังหวัด</label>
                                <div class="control">
                                    <input class="input" type="text" placeholder="Ex. สมุทรสงคราม">
                                  </div>
                            </div>
                                <div class="field is-grouped" id="MY">
                                  <div class="field" id="month">
                                      <label  id="text" class="label">เดือนหมดอายุ</label>
                                      <div class="control ">
                                          <input id="box" class="input" type="text" placeholder="mm" style="width: 70px;  margin-right: 48px;">
                                      </div>
                                  </div>
                                  <div class="field" id="year">
                                      <label  id="text" class="label">ปีหมดอายุ</label>
                                      <div class="control">
                                          <input id="box" class="input" type="text" placeholder="yyyy" style="width: 70px;">
                                      </div>
                                  </div>
                                </div>    
                                <div class="field" id="CVV">
                                    <label  id="text" class="label ">รหัสรักษาความปลอดภัย</label>
                                    <div class="control">
                                        <input class="input" type="text" placeholder="CVV">
                                    </div>
                                </div>
                                <div class="field is-horizontal">
                                    <div class="field">
                                        <div class="field is-expanded">
                                            <div class="field" id="postnumber">
                                                <label id="text"  class="label">หมายเลขไปรษณีย์</label>
                                                <div class="control">
                                                    <input class="input" type="text" placeholder="Ex.14140">
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="column is-11 is-offset-1">
                                    <footer id= "footer" class="modal-card-foot" >
                                        <button class="button ">ยกเลิก</button>
                                        <button class="button is-success">บันทึก</button>
                                    </footer>
                                </div>
                          </div>    
                      </div>
                  </section>
              </div>
          </div>
      </div>

        <!-- popupAddress -->
      <div class="modal-card" id="popUpAddress">
          <div class="container" >
              <div class="modal" id="page-modal2" >
                <div class="modal-background"></div>
                    <section class="modal-card-body">
                        <div class="modal-content" id="screenAddress">
                            <header id ="head" class="modal-card-head">
                                <p class="modal-card-title">ส่งสินค้าไปที่</p>
                                <button class="delete"  aria-label="close"></button>
                            </header>
                            <div class="columns is-multiline" style=" display: flex;" id="bodyPopUpAddress">
                                <div class="field is-horizontal" id="addressbox">
                                    <div class="field" >
                                        <label class="label">ชื่อ - นามสกุล</label>
                                        <div class="control">
                                            <input id="Name" class="input" type="text" placeholder="Ex. กิตฮับ ขยันอัพจัง" style="width: 300px;">
                                        </div>
                                    </div>
                                    <div class="field" style="margin-left: 60px;">
                                        <label class="label">หมายเลขโทรศัพท์ (สำหรับติดต่อ)</label>
                                        <div class="control">
                                            <input id="telNo" class="input" type="text" placeholder="Ex. 062-0672928 " style="width: 300px;" >
                                        </div>
                                    </div>
                                </div>
                                    <div class="field" id="addressbox-line2">
                                        <label class="label">ที่อยู่ในการจัดส่ง</label>
                                        <div class="control">
                                            <textarea class="textarea" id="address" placeholder="Ex. เช่น 112/44 ตึกหอสมุด ด้านใน KMUTT ถนนสุขสบายดี ตำบลมะละกอ" style="height: 100px; width: 300px;"></textarea>
                                        </div>
                                    </div>
                                    <div class="field" style="margin-left: 400px; margin-top: 100px;">
                                        <label class="label">จังหวัด</label>
                                        <div class="control">
                                            <input id="province" class="input" type="text" placeholder="Ex. กรุงเทพมหานคร " style="width: 300px; height: 50px;">
                                        </div>
                                    </div>
                                    <div class="field" style="margin-left: 400px; margin-bottom: 2000px;">
                                        <label class="label">หมายเลขไปรษณีย์</label>
                                        <div class="control">
                                            <input id="postcode" class="input" type="text" placeholder="Ex. 10140 " style="width: 300px; height: 50px;">
                                        </div>
                                    </div>
                                        
                            </div>
                            <div class="field is-grouped" id="buttonAddress">
                                    <footer id= "footer" class="modal-card-foot" >
                                        <button class="button" style="width: 100px;">ยกเลิก</button>
                                        <button class="button is-success" style="width: 100px; margin-left: 10px;">บันทึก</button>
                                    </footer>
                                </div>
                    </div>
                  </section>
                  
              </div>
          </div>
      </div>
    </div>
</template>

<script>
import './../../node_modules/bulma/css/bulma.css';

export default {
  name: 'ProductDetail',
  data () {
    return {
      msg: 'This is Detail page'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


#nav-bot {
    height: 240px;
}

#nav-bot-box {
    width: 1000px;
}

#nav-top {
  border-bottom: 10px;
  border-color: #E0E0E0;
}

#nav-box {
  width: 1000px;
}

#home-box {
  background: white;
  width: 1000px;
  min-height: 2000px;
  margin-top: 13px;
  box-shadow: 2px 10px grey;
}
html {
  background: #f2f2f2;
}

nav {
  background: #f2f2f2;
  border-bottom: 10px;
  border-color: #e0e0e0;
}

#nav-top {
  border-bottom: 10px;
  border-color: #e0e0e0;
}

#nav-box {
  width: 1000px;
}

/* popup */
#home-box {
  background: white;
  width: 1000px;
  min-height: 2000px;
  margin-top: 13px;
  box-shadow: 2px 10px grey;
}

#bodyPopUp {
  justify-content: center;
  background: white;
  margin-top:0px;
  margin-left: 0px;
  position: fixed;
  height: 606px;
  width: 299.5px;
}

#screen {
  width: 300px;
}

#addressbox {
    margin-top: 20px;
    margin-left: 40px;
    position: fixed;
}

#addressbox-line2 {
    margin-top: 100px;
    margin-left: 40px;
    position: fixed;
}

#bodyPopUpAddress {
    text-align: left;
    background: white;
    margin-top:0px;
    margin-left: 0px;
    position: fixed;
    height: 400px;
    width: 800px;
}

#screenAddress {
  width: 800px;
}

#buttonAddress {
    justify-content: center;
    margin-top: 300px;
    margin-right: 60px;
}
#box {
  width: 40%;
  height: 20%;
}

#text {
  font-size: 9pt;
  font-weight: 100;
}
#number{
    height: 9px;
    margin-right: 70px;
    margin-top: 10px;
}
#head{
    border-style: none;
    margin-top: 20px;
}
#footer{
    margin-left: 20px;
    background-color:white; 
    border-style: none;
}
</style>
