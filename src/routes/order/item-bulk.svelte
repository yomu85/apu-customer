<svelte:head>
  <title>주문벌크 | 고객사</title>
</svelte:head>

<!-- 페이지영역 -->
<main class="contents">
  <div class="con_title">
    <h3>주문벌크</h3>
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
          테스트
        </th> 
        <td>
          <span class="disabled">N</span>
        </td> 
        <th scope="row">
          준비중
        </th>
        <td>
          <span class="disabled">N</span>
        </td>
      </tr>
      </tbody>
    </table>
  </div>
     
  <div class="wj-content_wrap">
    <!-- wijmo area -->
    <div id="contentGridEl" class="wj-control wj-content wj-flexgrid" style="position: relative;">
      <div style="position: absolute; top: 50%; transform: translateY(-50%); width: 100%; height: auto; font-size:50px; text-align: center;">
        wijmo area
      </div>
    </div>
    <!-- //wijmo area -->
  </div>
</main>
<!-- //페이지영역 -->