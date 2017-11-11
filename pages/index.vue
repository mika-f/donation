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
      <div class="coinhive-miner" style="width: 100%; height: 320px" data-key="Zq1Z4osTwXAiSnpMAOCk6D71q9o9BLxr" data-autostart="false" data-whitelabel="false" data-background="#fafafa" data-text="#000000" data-action="#1e9ee0" data-graph="#1e9ee0" data-threads="4" data-throttle="0.1" data-start="Start Now!">
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
        {
          name: "Bitcoin",
          address: "1Gvd71AtuDRfkLkfpXcZtAantwJUjYv3tN",
          schema: "bitcoin"
        },
        {
          name: "Bitcoin Cash",
          address: "32ctqTga55CcV84kY9WHUMKZwjSJBMGJfH",
          schema: ""
        },
        {
          name: "BitCore",
          address: "15PseUcuyrZ1uRTJHCCeDBkj9P5dFdnMhP",
          schema: "bitcore"
        },
        {
          name: "BitZeny",
          address: "ZbVpLYsDGGmNvKUzx7YRQm3MWpENQ19DNg",
          schema: "bitzeny"
        },
        {
          name: "Blackcoin",
          address: "BSC9NPfCrFrRkfFiFzbmZ3PAhuX5GSEKQ7",
          schema: "blackcoin"
        },
        {
          name: "Dash",
          address: "XqAr2j1pTj34Yc9nLLsLCyFeEH9o32ghgf",
          schema: "dash"
        },
        {
          name: "Dogecoin",
          address: "D7Ydsu2TWWjdSaV1zfg9y8Y9Z4KJzh4ucp",
          schema: "dogecoin"
        },
        {
          name: "Litecoin",
          address: "LVUiYNgvaynAvCYN45tjojGSfuWd2BSfUj",
          schema: "litecoin"
        },
        {
          name: "Monacoin",
          address: "MC4x87u1ffmhsRhHof1sHz8UAtNtKCTQut",
          schema: "monacoin"
        },
        {
          name: "Peercoin",
          address: "PG8Ja96Th6mpwjDhTTQcmokzfbR5ZeZmk6",
          schema: "peercoin"
        },
        {
          name: "Primecoin",
          address: "AYMwtLDjxMmWsUctYH7AX27bFkKn5Dby3d",
          schema: "primecoin"
        }
      ]
    };
  },
  head: {
    link: [
      {
        rel: "stylesheet",
        href:
          "https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta/css/bootstrap.min.css"
        // integrity: 'sha384-/Y6pD6FV/Vv2HJnA6t+vslU6fwYXjCFtcEpHbNJ0lyAFsXTsjBbfaDjzALeQsN6M',
        // crossorigin: 'anonymous'
      }
    ]
  }
};
</script>

<style>
section {
  padding: 10px 0 20px 0;
}
</style>
