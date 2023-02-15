<script>
import { page } from  "$app/stores"
import gnbData from "$lib/data/gnb.json"

//$: console.log('pathname: ', $page.url.pathname)
const menus = gnbData

</script>
<header id="header">
  <div class="topmenu">
    <div class="util">
      <a href="https://apuo.arong.day/" class="btn btn-dark">Go 운영사</a>
    </div>
  </div>
  <div class="gnb_area">
    <h1>
      <a href="/">
        <img src="/static/images/allt_logo_white.svg" alt="allt">
        <span>고객사</span>
      </a> 
    </h1> 
    <nav>
      <ul class="gnb_list">
        {#each menus as menu}
          <li class:active={$page.url.pathname.startsWith(menu.path)}>
            <a href={menu.href}>{menu.name}</a>
          </li>
        {/each}
        <!-- <li class:active={$page.url.pathname.startsWith('/admin')}>
          <a href="/admin/budget">환경설정</a>
        </li>
        <li class:active={$page.url.pathname.startsWith('/order')}>
          <a href="/order/prod_inquiry" >주문관리</a>
        </li> -->
      </ul>
    </nav>
  </div>
</header>

{#if $page.url.pathname === '/'}
<aside id="aside">
  <h2>APU 홈</h2>
</aside>
{:else}
<aside id="aside">
  {#each menus as menu}
    {#if $page.url.pathname.startsWith(menu.path)}
      <h2>{menu.name}</h2>
      <ul class="lnb_list">
        {#each menu.subMenus as sub}
          <li class:active={$page.url.pathname.startsWith(sub.href)}>
            <a href={sub.href}>{sub.name}</a>
          </li>
        {/each}
      </ul>
    {/if}
  {/each}
  <!-- {#if $page.url.pathname.startsWith('/admin')}
    <h2>환경설정</h2> 
    <ul class="lnb_list">
      <li class:active={$page.url.pathname === '/admin/budget'} 
      ><a href="/order/prod_inquiry">예산관리</a></li>
    </ul>
  {:else if $page.url.pathname.startsWith('/order')}
    <h2>주문관리</h2> 
    <ul class="lnb_list">
      <li class:active={$page.url.pathname === '/order/prod_inquiry'} 
      ><a href="/order/prod_inquiry">상품조회</a></li>
      <li class:active={$page.url.pathname === '/order/cart'} 
      ><a href="/order/cart">장바구니</a></li>
      <li class:active={$page.url.pathname === '/order/order_bulk'} 
      ><a href="/order/order_bulk">주문벌크</a></li>
      <li class:active={$page.url.pathname === '/order/order_inquiry'} 
      ><a href="/order/order_inquiry">주문조회</a></li>
    </ul>
  {/if} -->
</aside>
{/if}

<style scoped>
#header {
  min-width: 120rem;
}
#header .topmenu {
  display: flex;
  justify-content: flex-end;
  height: 3.5rem;
  padding: .5rem  2rem;
  background: #013360;
}
#header .topmenu .util .btn {
  width: 8rem;
  height: 2.5rem;
  line-height: 2;
  padding-left: 1.5rem;
  background: #012749 url(/static/images/icon/icon_out.gif) no-repeat 10% center;
  font-size: 1.1rem;
  font-weight: normal;
}
#header .gnb_area {
  display: flex;
  height: 5.4rem;
  padding: .9rem 4rem .9rem 0;
  background: #012749;
}
#header h1 {
  width: 19rem;
  text-align: center;
  position: relative;
  top: -1px;
}
#header h1 img {
  height: 1.6rem;
}
#header h1 span {
  position: relative;
  top: -1px;
  font-size: 1.3rem;
  font-weight: normal;
  color: #fff;
}
#header nav {
  position: relative;
  top: 1px;
  margin-left: 2.2rem;
}
#header nav .gnb_list {
  display: flex;
}
#header nav .gnb_list li {
  margin-left: 4.8rem;
}
#header nav .gnb_list li:first-child {
  margin-left: 0;
}
#header nav .gnb_list li a {
  font-size: 1.3rem;
  letter-spacing: 0;
  line-height: 3.6rem;
  color: #fff;
}
#header nav .gnb_list li a:active,
#header nav .gnb_list li a:hover,
#header nav .gnb_list li a:focus,
#header nav .gnb_list li.active a {
  color: #A6C8FF
}

#aside {
  position: absolute;
  top: 8.9rem;
  left: 0;
  width: 19rem;
  min-height: calc(100vh - 8.9rem);
  background: #fff;
}
#aside h2 {
  height: 5rem;
  background: #EDF5FF;
  line-height: 5rem;
  font-size: 1.4rem;
  font-weight: bold;
  color: #003A6D;
  text-align: center;
}
#aside .lnb_list li {
  border-bottom: 1px solid #e3e8eb
}
#aside .lnb_list li a {
  display: block;
  padding: 1.5rem 2rem;
  font-size: 1.3rem;
  font-weight: normal;
  color: #343a3f;
}
#aside .lnb_list li a:active,
#aside .lnb_list li a:hover,
#aside .lnb_list li a:focus,
#aside .lnb_list li.active a {
  color: #292929;
  font-weight: bold;
}
</style>