<svelte:head>
  <title>예산관리 | 고객사</title>
</svelte:head>

<script>
// import { onMount } from 'svelte';

// onMount(() => {
//   (function( $ ) {
//     $('#transferedbudgetModal').modal()
//   })(jQuery);
// });

function transferedbudgetModalToggle() {
  (function( $ ) {
    $('#transferedbudgetModal').modal()
  })(jQuery);
}
function divisionModalToggle() {
  (function( $ ) {
    $('#divisionModal').modal()
  })(jQuery);
}
function deptModalToggle() {
  (function( $ ) {
    $('#deptModal').modal()
  })(jQuery);
}
function accountModalToggle() {
  (function( $ ) {
    $('#accountModal').modal()
  })(jQuery);
}
</script>

<!-- 페이지영역 -->
<main class="contents">
  <div class="con_title">
    <h3>예산관리</h3>
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
            <label for="year">예산년월</label>
          </th> 
          <td>
            <div class="flex_box">
              <select name="year" id="year" required="required" class="form-control">
                <option value="2022">2022</option>
              </select> 
              <div class="frog">/</div>
              <select name="month" id="month" required="required" class="form-control frog">
                <option value="1">1</option>
                <option value="2">2</option>
              </select>
            </div>
          </td> 
          <th scope="row">
            <label for="division">사업부</label>
          </th>
          <td>
            <select name="division" id="division" required="required" class="form-control">
              <option value="45">관리부서</option>
            </select>
          </td>
        </tr> 
        <tr>
          <th scope="row">
            <label for="dept">부서명</label>
          </th> 
          <td>
            <select name="dept" id="dept" required="required" class="form-control"></select>
          </td> 
          <th scope="row">
            <label for="accounts">계정명</label>
          </th> 
          <td>
            <select name="accounts" id="accounts" required="required" class="form-control">
              <option value="14">사무용품</option>
            </select>
          </td>
        </tr>
      </tbody>
    </table>
    <div class="btn_box">
      <button type="button" class="btn btn-secondary line">초기화</button>
      <button type="button" class="btn btn-secondary">조회</button>
    </div>
  </div>

  <div class="wj-content_wrap">
    <div class="btn_box between">
      <div class="flex_box">
        <button type="button" class="btn btn-light">저장</button>
        <button type="button" class="btn btn-light">삭제</button>
        <button type="button" class="btn btn-light" on:click={transferedbudgetModalToggle}>
          예산 이월
        </button>
      </div>
      <div class="flex_box">
        <button type="button" class="btn btn-light">
          Excel 가져오기
        </button>
        <button type="button" class="btn btn-light">
          Excel 내보내기
        </button>
      </div>
    </div>

    <!-- wijmo area -->
    <div id="contentGridEl" class="wj-control wj-content wj-flexgrid" style="position: relative;">
      <div style="position: absolute; top: 50%; transform: translateY(-50%); width: 100%; height: auto; font-size:50px; text-align: center;">
        wijmo area
        <div class="btn_box">
            <button type="button" class="btn btn-light" on:click={divisionModalToggle}>
                사업부 입력
            </button>
            <button type="button" class="btn btn-light" on:click={deptModalToggle}>
                부서 입력
            </button>
            <button type="button" class="btn btn-light" on:click={accountModalToggle}>
                계정 입력
            </button>
        </div>
      </div>
    </div>
    <!-- //wijmo area -->

    <div class="btn_box right mt_half">
      <button type="button" class="btn btn-light">
        행추가
      </button>
    </div>
  </div>
</main>
<!-- //페이지영역 -->

<!-- 예산 이월 입력 Modal -->
<div class="modal fade" id="transferedbudgetModal" tabindex="-1" role="dialog" aria-labelledby="transferedbudgetModalTitle"
  aria-hidden="true">
  <div class="modal-dialog modal_sm modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="transferedbudgetModalTitle">예산 이월</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt=""></span>
        </button>
      </div>
      <div class="modal-body">
        <table class="table_line">
          <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
          <colgroup>
            <col style="width: 25%">
            <col style="width: 75%">
          </colgroup>
          <tbody>
            <tr>
              <th scope="row">
                <label for="transferedReqUserName">요청자</label>
              </th>
              <td>
                <input type="text" class="form-control" id="transferedReqUserName">
              </td>
            </tr>
            <tr>
              <th scope="row">
                <label for="transferedReason">이월사유</label>
              </th>
              <td>
                <input type="textarea" class="form-control" id="transferedReason">
              </td>
            </tr>
            
          </tbody>
        </table>
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">닫기</button>
        <button type="button" class="btn btn-secondary">저장</button>
      </div>
    </div>
  </div>
</div>

<!-- 사업부 입력 Modal -->
<div class="modal fade" id="divisionModal" tabindex="-1" role="dialog" aria-labelledby="divisionModalTitle"
  aria-hidden="true">
  <div class="modal-dialog modal_sm modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="divisionModalTitle">사업부 입력</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt=""></span>
        </button>
      </div>
      <div class="modal-body">
        <select class="form-control" id="divisionModalSelect" style="width: 384px">
          <option value="0" selected>----선택----</option>
        </select>
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">닫기</button>
        <button type="button" class="btn btn-secondary">저장</button>
      </div>
    </div>
  </div>
</div>

<!-- 부서 입력 Modal -->
<div class="modal fade" id="deptModal" tabindex="-1" role="dialog" aria-labelledby="deptModalTitle"
  aria-hidden="true">
  <div class="modal-dialog modal_sm modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="deptModalTitle">부서 입력</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt=""></span>
        </button>
      </div>
      <div class="modal-body">
        <select class="form-control" id="deptModalSelect" style="width: 384px">
          <option value="0" selected>----선택----</option>
        </select>
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">닫기</button>
        <button type="button" class="btn btn-secondary">저장</button>
      </div>
    </div>
  </div>
</div>

<!-- 계정 입력 Modal -->
<div class="modal fade" id="accountModal" tabindex="-1" role="dialog" aria-labelledby="accountModalTitle" aria-hidden="true">
  <div class="modal-dialog modal_sm modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="accountModalTitle">계정 입력</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt=""></span>
        </button>
      </div>
      <div class="modal-body">
        <select class="form-control" id="accountModalSelect" style="width: 384px">
          <option value="0" selected>----선택----</option>
        </select>
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">닫기</button>
        <button type="button" class="btn btn-secondary">저장</button>
      </div>
    </div>
  </div>
</div>

<style>
  .wj-content_wrap {
    height: calc(100% - 20rem);
  }
</style>