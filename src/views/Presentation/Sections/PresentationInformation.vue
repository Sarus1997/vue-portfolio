<script setup>
import RotatingCard from "../../../examples/cards/rotatingCards/RotatingCard.vue";
import RotatingCardFront from "../../../examples/cards/rotatingCards/RotatingCardFront.vue";
import RotatingCardBack from "../../../examples/cards/rotatingCards/RotatingCardBack.vue";
import DefaultInfoCard from "../../../examples/cards/infoCards/DefaultInfoCard.vue";
</script>
<template>
  <section class="my-5 py-5">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-4 ms-auto me-auto p-lg-4 mt-lg-0 mt-4">
          <RotatingCard>
            <RotatingCardFront
              image="https://images.unsplash.com/photo-1569683795645-b62e50fbf103?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80"
              title="สหรัฐ สุวรรณภาพร"
              description="เป็นนักศึกษาของมหาวิทยาลัยวลัยลักษณ์ วิทยาศาสตรบัณฑิต สาขาเทคโนโลยีสารสนเทศและนวัตกรรมดิจิทั"
            />

            <RotatingCardBack
              image="https://images.unsplash.com/photo-1498889444388-e67ea62c464b?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1365&q=80"
              title="ข้อมูลแบบย่อ"
              description="ชื่อเล่น : ซารุส, 
              ปีเกิด : 10/06/1997, 
              งานอดิเรก : เล่นเกม , ทำอาหาร"
            />
          </RotatingCard>
        </div>
        <div class="col-lg-6 ms-auto">
          <br />
          <div class="row justify-content-start">
            <DefaultInfoCard
              icon="content_copy"
              title="มหาวิทยาลัย"
              description="มหาวิทยาลัยวลัยลักษณ์"
            />
            <DefaultInfoCard
              icon="flip_to_front"
              title="คณะ"
              description="สารสนเทศศาสตร์"
            />
          </div>
          <div class="row justify-content-start mt-5">
            <DefaultInfoCard
              class="mt-3"
              icon="price_change"
              title="สาขา"
              description="เทคโนโลยีสารสนเทศและนวัตกรรมดิจิทั"
            />
            <DefaultInfoCard
              class="mt-3"
              icon="devices"
              title="GPAX"
              description="3.17"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
