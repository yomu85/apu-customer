<svelte:head>
  <title>장바구니 | 고객사</title>
</svelte:head>

<script>
// import Loader from '$lib/Loader.svelte'
let loading = false;

function loadingToggle() {
  loading = !loading
}
</script>

<!-- 페이지영역 -->
<main class="contents">
  <div class="con_title">
    <h3>장바구니</h3>
  </div>

  <button type="button" class="btn btn-light btn_srch" data-toggle="collapse" data-target="#srch_area" aria-controls="srch_area" aria-expanded="false">
    <img src="/static/images/icon/arr_srch.png" alt="검색창 여닫이">
  </button>
  <div class="srch_area collapse show" id="srch_area">
    <table class="table_line">
      <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
      <colgroup>
        <col style="width: 10%">
        <col style="width: 40%">
        <col style="width: 10%">
        <col style="width: 40%">
      </colgroup>
      <tbody>
      <tr>
        <th scope="row">
          결제여부
        </th> 
        <td>
          <span class="disabled">N</span>
        </td> 
        <th scope="row">
          예산체크
        </th>
        <td>
          <span class="disabled">N</span>
        </td>
      </tr>
      </tbody>
    </table>

    <table class="table_line mt16">
      <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
      <colgroup>
        <col style="width: 10%">
        <col style="width: 40%">
        <col style="width: 10%">
        <col style="width: 40%">
      </colgroup>
      <tbody>
      <tr>
        <th scope="row">
          주문자
        </th> 
        <td>
          <span class="disabled">김준휘</span>
        </td> 
        <th scope="row">
          주문자 부서
        </th>
        <td>
          <span class="disabled">관리팀</span>
        </td>
      </tr>
      <tr>
        <th scope="row">
          연락처
        </th> 
        <td>
          <span class="disabled">043-879-9161</span>
        </td> 
        <th scope="row">
          휴대폰
        </th>
        <td>
          <span class="disabled">010-4168-9161</span>
        </td>
      </tr>
      <tr>
        <th scope="row">
          선입고여부
        </th> 
        <td>
          <div class="chk_label">
            <input type="checkbox" class="form-control" id="chk_prearrival">
            <label for="chk_prearrival">선입고</label>
          </div>
        </td> 
        <th scope="row">
          주문일자
        </th>
        <td>
          <input type="date" value="2022-06-17" class="form-control">
        </td>
      </tr>
      </tbody>
    </table>
  </div>
     
  <div class="wj-content_wrap">
    <h4>장바구니 목록</h4>
    <ul class="page_tablist">
      <li><a href="/order/item-cart">상품목록</a></li>
      <li class="active"><a href="/order/item-cart2">주문서목록</a></li>
    </ul>
    <div class="btn_box between">
      <div class="flex_box">
        <strong class="txt_cost_bold">Total : KRW 24,730</strong>
        <span class="txt_cost">(부가세별도)</span>
      </div>
      <div class="flex_box">
        <button type="button" class="btn btn-light" id="loadingActive" on:click={loadingToggle}>{loading ? '주문취소' : '주문'}</button>
        <button type="button" class="btn btn-light">Excel 다운로드</button>
        <button type="button" class="btn btn-light">삭제</button>
        <button type="button" class="btn btn-light">주문</button>
      </div>
    </div>

    <!-- wijmo area -->
    <div id="contentGridEl" class="wj-control wj-content wj-flexgrid" style="position: relative;">
      wijmo area
      {#if loading}
        <!-- 로딩 영역 -->
        <div class="loading_circle">
          <div class="sk-fading-circle">
            <div class="sk-circle1 sk-circle"></div>
            <div class="sk-circle2 sk-circle"></div>
            <div class="sk-circle3 sk-circle"></div>
            <div class="sk-circle4 sk-circle"></div>
            <div class="sk-circle5 sk-circle"></div>
            <div class="sk-circle6 sk-circle"></div>
            <div class="sk-circle7 sk-circle"></div>
            <div class="sk-circle8 sk-circle"></div>
            <div class="sk-circle9 sk-circle"></div>
            <div class="sk-circle10 sk-circle"></div>
            <div class="sk-circle11 sk-circle"></div>
            <div class="sk-circle12 sk-circle"></div>
          </div>
        </div>
        <!-- //로딩 영역 -->
      {/if}
    </div>
    <!-- //wijmo area -->
  </div>
</main>
<!-- //페이지영역 -->