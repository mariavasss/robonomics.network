<template>
  <layout>

    <MetaInfo
      :pageTitle = "'Community'"
      :pageDescription = "'On this page you may find logo assets, wallpapers, documents such as White Paper, links to our scientific papers, social account, read about Robonomics Utility Token (XRT), and dig out other useful information.'"
      :pageImage = "'/website_cover_community.png'"
    />

    <div class="layout__title">
      <h1>Robonomics community</h1>
    </div>

    <section class="layout layout__text">

      <tabs>

          <tab name="Docs" :selected="true">
              <share :assets="docs"/>
          </tab>

          <tab name="Token">

              <p class="hyphens"><strong>There are 2 tokens in Robonomics for now: XRT and RWS. Please, research the information below carefully before buying or asking questions in Community. You are welcome!</strong></p>


              <div class="section oldy token">
                <div class="section token__title">
                  <img alt="Robonomics token, XRT image" src="/Robonomics-Token-XRT-color.svg" class="token__sign"/>
                  <h2>Robonomics token, XRT</h2>
                </div>

                <div class="section">
                    <h3>Token address:</h3>
                    <ul>
                      <li class="line-text">
                        <g-link class="inline-block button primary small" to="https://etherscan.io/address/0x7de91b204c1c737bcee6f000aaa6569cf7061cb7">Etherscan:</g-link>
                        <IconCopy class="inline-block" address="0x7de91b204c1c737bcee6f000aaa6569cf7061cb7"/>
                        <code class="address inline-block">0x7de91b204c1c737bcee6f000aaa6569cf7061cb7</code>
                    
                      </li>
                      <li class="line-text">
                        <g-link class="inline-block button primary small" to="https://bscscan.com/token/0xc0a51ac9d548bdcde53fa59448029e41a39feb20">BscScan:</g-link>
                        <IconCopy class="inline-block" address="0xc0a51ac9d548bdcde53fa59448029e41a39feb20"/> 
                        <tip summary="☝️" position="center-bottom" class="inline-block">
                          This token contract is maintained by the <g-link to="https://anyswap.exchange/dashboard">anyswap.exchange team</g-link>. The Robonomics team is not responsible for the issuance of the token in the Binance Smart Chain.
                        </tip>
                        <code class="address inline-block">0xc0a51ac9d548bdcde53fa59448029e41a39feb20</code>
                        
                      </li>
                    </ul>
                </div>

                <div class="section">
                  <h3>XRT/ETH pair:</h3>

                  <div class="line-text">
                    <g-link class="button border" to="https://uniswap.info/pair/0x3185626c14acb9531d19560decb9d3e5e80681b1">Uniswap</g-link>
                    <g-link class="button border" to="https://www.huobi.com/ru-ru/exchange/xrt_eth/">Huobi</g-link>
                    <g-link class="button border" to="https://www.coingecko.com/en/coins/robonomics-network/">Сoingecko</g-link>
                  </div>
                </div>

                <div class="section">
                  <h3>Quick intro to XRT:</h3>
                  <p><g-link class="button border" to="https://ipfs.io/ipfs/QmYjv65UNTM3F7LFR1ESm5CVMLWYLagwtT7qGAsaBi47nY/releases_March'21_4v.pdf">Distribution Release March 2021</g-link></p>
                  <p><g-link to="https://static.robonomics.network/docs/whitepaper/Robonomics-whitepaper-en.pdf">Theory in White Paper, Chapter 6</g-link></p>
                  <p><g-link to="https://blog.aira.life/robonomics-x-pancakeswap-buy-and-add-liquidity-on-pancakeswap-a1b87ef9cb99">Buy and Add Liquidity on PancakeSwap</g-link></p>
                </div>
              </div>


              <div class="section oldy token">
                <div class="section token__title">
                  <img alt="Robonomics Web Services, RWS image" src="/Robonomics-Token-RWS-color.svg" class="token__sign"/>
                  <h2>RWS Lifetime Subscription</h2>
                </div>

                <div class="section">
                    <h3>Token address:</h3>
                    <p class="line-text">
                      <g-link class="inline-block button primary small" to="https://etherscan.io/address/0x08ad83d779bdf2bbe1ad9cc0f78aa0d24ab97802">Etherscan:</g-link>
                      <IconCopy class="inline-block" address="0x08ad83d779bdf2bbe1ad9cc0f78aa0d24ab97802"/>
                      <code class="inline-block address">0x08ad83d779bdf2bbe1ad9cc0f78aa0d24ab97802</code>
                      
                    </p>
                </div>

                <div class="section">
                    <h3>RWS/XRT pair:</h3>
                    <g-link class="button border" to="https://uniswap.info/pair/0x42018a2ff89b6d662b5f746277bd02f0d85f485a">Uniswap</g-link>
                </div>

                <div class="section">
                    <h3>Quick intro to RWS:</h3>
                    <p><g-link to="https://blog.aira.life/robonomics-web-services-and-rws-token-intro-d730ab50ad42">Robonomics Web Services and RWS token intro</g-link></p>
                    <p><g-link to="https://blog.aira.life/rws-overview-part-2-heterogeneous-tokenomics-afc209cc855">RWS overview, part 2 “Heterogeneous tokenomics”</g-link></p>
                </div>
              </div>

              <section>
                <h2>Beware of scammers</h2>
                <ol>
                  <li>Check the address of token while buying. Do not copy the address from chats or any private messages, view it on Etherscan.</li>
                  <li>Please, check the information about rewards from official channels: <g-link to="https://www.robonomics.events/#/">robonomics.events</g-link> or <g-link to="https://twitter.com/AIRA_Robonomics">Twitter</g-link></li>
                  <li>Robonomics (robonomics.network) and / or the AIRA (Airalab) team member WILL NOT send you any personal messages before you ask yourself for our help. Beware of messages containing any fake addresses or asking you personal data.</li>
                </ol>
              </section>

            </tab>

          <tab name="Science">
              <share :assets="science" :classes="'tab-science'"/>
          </tab>

          <tab name="Assets">
            <share :assets="assets"/>
          </tab>

          <tab name="Intouch">
            <share :assets="intouch" :classes="'tab-intouch'"/>
          </tab>
      </tabs>
    </section>

  </layout>
</template>


<script>
  import assets from '@/data/assets.yaml'
  import docs from '@/data/docs.yaml'
  import science from '@/data/science.yaml'
  import intouch from '@/data/intouch.yaml'

  export default {

    components: {
      MetaInfo: () => import('~/components/MetaInfo.vue'),
      share: () => import('~/components/Share.vue'),
      tabs: () => import('~/components/tabs.vue'),
      tab: () => import('~/components/tab.vue'),
      IconCopy: () => import('~/components/IconCopy.vue'),
      tip: () => import('~/components/tip.vue'),
    },


    computed: {
      assets () {
        return assets
      },
      docs () {
        return docs
      },
      science () {
        return science
      },
      intouch () {
        return intouch
      }
    }

  }

</script>


<style lang="scss">

  .address {
    word-break: break-word;
    overflow-wrap: break-word;
  }


  .token {
    padding: var(--space);
    text-align: center;

    &__sign {
      display: block;
      max-width: 100%;
      width: 10rem;
      margin: 0 auto calc(var(--space)/2);
    }

    .section {
      padding: calc(var(--space)/2) 0 var(--space-text);

      &:not(:last-child) {
        border-bottom: 2px dotted var(--color-dark);
      }
    }

    h2, h3 {
      margin-top: 0;
    }

    ul {
      list-style: none;
      margin-left: 0;
    }

    li {
      margin-bottom: calc(var(--space-text)/2);
    }
  }

  @media screen and (max-width: 600px) {
    .token {
      text-align: left;

      &__title {
        display: grid;
        grid-template-columns: 3rem 3fr;
        gap: calc( var(--space)/2 );
        align-items: center;

        h4 { margin: 0; }
      }

      .section {
        &:first-child { margin-top: 0; }
        &:last-child { margin-bottom: 0; }
      }
    }
  }

</style>
