#var truewallet = require('./apis/truewallet');

// ข้อมูลที่ระบุ
var senderPhoneNumber = '0840075274';  // เบอร์โทรศัพท์ผู้โอน
var recipientPhoneNumber = '0639067292';  // เบอร์โทรศัพท์ผู้รับ
var amount = 63000.01;  // จำนวนเงินที่คืนจากโปรโมชั่น
var transactionReference = '50036784744660';  // เลขอ้างอิงการทำรายการ
var transactionDate = '20/12/2567';  // วันที่ทำรายการ
var transactionTime = '00:04:00';  // เวลา 12:04 AM หรือ 00:04:00

// ตัวอย่างการเรียก API เพื่อทำการโอนหรือแลกคูปอง
truewallet.redeemvouchers(senderPhoneNumber, transactionReference)
.then(res => {
    if (res.status === 'SUCCESS') {
        console.log('การทำรายการสำเร็จ จำนวนเงินที่ได้รับ: ' + res.amount);
        conso
