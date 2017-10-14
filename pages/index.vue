<template>
  <div class="container">
    <h1>寄付</h1>
    <section>
      <p>
        もし、私の作ったアプリを気に入ってくれたなら、下記アドレスから、暗号通貨を寄付することが出来ます！
      </p>
      <p>
        <small>
          ※寄付された暗号通貨の使い道については、お答えすることはできません。
        </small>
      </p>
      <table>
        <tbody>
          <tr v-for="w in addresses" :key="w.address">
            <td>{{w.name}}</td>
            <td>
              <a :href="`${w.schema}:${w.address}`">{{w.address}}</a>
            </td>
          </tr>
        </tbody>
      </table>
    </section>
    <section>
      <p>もしくは、マシンの CPU パワーを使って、寄付することもできます。</p>
      <div class="coinhive-miner" style="width: 256px; height: 310px" data-key="Zq1Z4osTwXAiSnpMAOCk6D71q9o9BLxr" data-autostart="false" data-whitelabel="false" data-background="#000000" data-text="#eeeeee" data-action="#00ff00" data-graph="#555555" data-threads="1" data-throttle="0.1" data-start="Start Now!">
        <em>Please disable Adblock!</em>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      addresses: [
        { name: 'Bitcoin', address: '1Gvd71AtuDRfkLkfpXcZtAantwJUjYv3tN', schema: 'bitcoin' },
        { name: 'BitZeny', address: 'ZbVpLYsDGGmNvKUzx7YRQm3MWpENQ19DNg', schema: 'bitzeny' },
        { name: 'Dash', address: 'XqAr2j1pTj34Yc9nLLsLCyFeEH9o32ghgf', schem: 'dash' },
        { name: 'Litecoin', address: 'LVUiYNgvaynAvCYN45tjojGSfuWd2BSfUj', schema: 'litecoin' },
        { name: 'Monacoin', address: 'MC4x87u1ffmhsRhHof1sHz8UAtNtKCTQut', schema: 'monacoin' }
      ]
    }
  },
  head: {
    script: [
      { type: 'text/javascrpt', src: 'https://coinhive.com/lib/miner.min.js', async: true }
    ]
  }
}
</script>

<style>
.container {
  padding-top: 24px;
  padding-bottom: 24px;
  margin-right: auto;
  margin-left: auto;
  padding-right: 15px;
  padding-left: 15px;
  width: 100%;
  min-height: 100vh;
  background-color: #f3f3f3;
  color: #333;
  font-family: "Open Sans", "Helvetica Neue", Helvetica, Arial, "游ゴシック", YuGothic, "ヒラギノ角ゴ ProN W3", "Hiragino Kaku Gothic ProN", "メイリオ", Meiryo, sans-serif;
}

section {
  padding: 10px 0 20px 0;
}

table {
  border-radius: 0;
  box-shadow: 0 3px 0 rgba(0, 0, 0, 0.04), 0 0 0 1px #E8E8E8 inset;
  margin-top: 10px;
  margin-bottom: 15px;
  overflow: hidden;
  border-spacing: 0;
  background: none repeat scroll 0 0 #FFF;
}

table thead {
  background: none repeat scroll 0 0 #298CC3;
  color: #FFFFFF;
}

table thead th {
  padding: 10px 15px;
  text-align: left;
}

table tbody td {
  border-bottom: 1px solid #E8E8E8;
  padding: 9px 15px;
}

table tbody tr:nth-child(2n+1) {
  background: none repeat scroll 0 0 #F7F7F7;
}
</style>
