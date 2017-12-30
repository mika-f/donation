<template>
  <div class="container">
    <h1>寄付</h1>
    <section>
      <p>
        もし、私の作ったアプリやサービスを気に入ってくれたなら、下記アドレスから、暗号通貨を寄付することが出来ます！ <br>
        <small>
          ※寄付された暗号通貨の使い道については、お答えすることはできません。 <br>
          ※単純に投げ銭でも嬉しいです。
        </small>
      </p>
      <div class="d-none d-sm-block">
        <div class="row">
          <div class="col-md-6">
            <table class="table table-bordered">
              <tbody>
                <tr v-for="w in addresses.filter((el, idx, arr) => idx % 2 == 0)" :key="w.address">
                  <th>{{w.name}}</th>
                  <td>
                    <code>{{w.address}}</code>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="col-md-6">
            <table class="table table-bordered">
              <tbody>
                <tr v-for="w in addresses.filter((el, idx, arr) => idx % 2 == 1)" :key="w.address">
                  <th>{{w.name}}</th>
                  <td>
                    <code>{{w.address}}</code>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
      <div class="d-block d-sm-none">
        <table style="table-layout: fixed;" class="table table-bordered table-responsive">
          <tbody>
            <tr v-for="w in addresses" :key="w.address">
              <th style="min-width: 150px">{{w.name}}</th>
              <td>
                <code>{{w.address}}</code>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
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
import sortBy from "lodash.sortby";

export default {
  data: () => {
    return {
      addresses: sortBy(
        [
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
          },
          {
            name: "XP",
            address: "XZvrWCPeHtzBAUx2P3fcwGCB5kSsfiXMc6",
            schema: "xp"
          },
          {
            name: "Ethereum",
            address: "0xDc48d5AF8dCa1284F8770553E6e01beeE510535D"
          },
          {
            name: "Ripple",
            address: "rUpRPeEwjkHwU4wyZKeFLRQQvCguxZP4UG"
          },
          {
            name: "Fujicoin",
            address: "FbSYmbpK1ZyrE3zUDTGcjf1sUDpq1DU7vV"
          },
          {
            name: "Nekonium",
            address: "0xAb18ea682305E4264C6F40Fb2F61a37FB847201f"
          },
          {
            name: "NEM",
            address: "NDXD3H-ZJVPEI-JDWA7Q-56DUKJ-3YYQZV-QHX7DL-GMDV"
          },
          {
            name: "Neo",
            address: "ALaiMeM3Je2ehPpwvBMuNGHaaYBWFe7de3"
          },
          {
            name: "ZCash",
            address: "t1MyEJt3HVaLAxm4tU1a8w5K1wWBLZXn79Q"
          },
          {
            name: "Ethereum Classic",
            address: "0xfd0859b6f00bee9777511c96cd3e86418390a99d"
          },
          {
            name: "Augur",
            address: "0x423a129b99d3a8be088dcec89878ca8dba67a775"
          },
          {
            name: "decred",
            address: "DskczKwMVSKHcwwVSLMPrJnRAPzQiqEW19Y"
          },
          {
            name: "NXT",
            address: "NXT-6UKG-V7TL-TA7C-4K3KP"
          }
        ],
        w => w.name.toLocaleLowerCase()
      )
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
