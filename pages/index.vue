<template>
  <div class="container">
    <h1>寄付</h1>
    <section>
      <p>
        もし、私の作ったアプリやサービスを気に入ってくれたなら、下記アドレスから、暗号通貨を寄付することが出来ます！ <br>
        <small>
          ※寄付された暗号通貨の使い道については、お答えすることはできません。
        </small>
      </p>
      <table class="table table-bordered">
        <tbody>
          <tr v-for="w in addresses" :key="w.address">
            <td>{{w.name}}</td>
            <td>
              <a :href="`${w.schema}:${w.address}`">
                <code>{{w.address}}</code>
              </a>
            </td>
          </tr>
        </tbody>
      </table>
    </section>
    <section>
      <p>もしくは、 Monero マイニングによる寄付をすることもできます。</p>
      <script src="https://coinhive.com/lib/miner.min.js" async></script>
      <div class="coinhive-miner" style="width: 728px; height: 90px" data-key="Zq1Z4osTwXAiSnpMAOCk6D71q9o9BLxr" data-autostart="false" data-whitelabel="false" data-background="#000000" data-text="#eeeeee" data-action="#00ff00" data-graph="#555555" data-threads="4" data-throttle="0.1" data-start="Start Now!">
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
        { name: 'Dash', address: 'XqAr2j1pTj34Yc9nLLsLCyFeEH9o32ghgf', schema: 'dash' },
        { name: 'Litecoin', address: 'LVUiYNgvaynAvCYN45tjojGSfuWd2BSfUj', schema: 'litecoin' },
        { name: 'Monacoin', address: 'MC4x87u1ffmhsRhHof1sHz8UAtNtKCTQut', schema: 'monacoin' }
      ]
    }
  },
  head: {
    link: [
      {
        rel: 'stylesheet',
        href: 'https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta/css/bootstrap.min.css'
        // integrity: 'sha384-/Y6pD6FV/Vv2HJnA6t+vslU6fwYXjCFtcEpHbNJ0lyAFsXTsjBbfaDjzALeQsN6M',
        // crossorigin: 'anonymous'
      }
    ]
  }
}
</script>

<style>
section {
  padding: 10px 0 20px 0;
}
</style>
