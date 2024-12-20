# Supported Chains and DEX

This page will list the supported chains and DEXs, along with integrations for those wishing to link back to Quick Intel.\
&#xNAN;_&#x4E;OTE: We are constantly adding/changing support for new chains and DEXs and all data is subject to change._

### Chains

<table><thead><tr><th width="238">Blockchain</th><th width="193.33333333333331">ID</th><th>DEXs/Honeypot Check ID</th></tr></thead><tbody><tr><td>Ethereum</td><td>eth</td><td>Uniswap V2 / uniswap2<br>Uniswap V3 / uniswap3<br>ShibaSwap / sushiswapeth</td></tr><tr><td>Arbitrum</td><td>arbitrum</td><td>SushiSwap / sushiswaparb<br>Camelot / camelotarb<br>TraderJoeV1 / traderjoev1arb<br>OreoSwap / oreoswaparb</td></tr><tr><td>Binance Smart Chain</td><td>bsc</td><td>PancakeSwap / pancakeswap</td></tr><tr><td>Polygon</td><td>polygon</td><td>QuickSwap /quickswappolygon</td></tr><tr><td>Fantom</td><td>fantom</td><td>SpookySwap / spookyswapfantom</td></tr><tr><td>Avalanche</td><td>avalanche</td><td>TraderJoeV1 / traderjoeavalanche<br>Pangolin / pangolinavalanche</td></tr><tr><td>Core DAO</td><td>core</td><td>ArcherSwap / archerswapcore<br>ShadowSwap / shadowswapcore<br>IceCreamSwap / icecreamswapcore<br>LFGSwap / lfgswapcore</td></tr><tr><td>zkSync</td><td>zksync</td><td>Mute / mutezksync</td></tr><tr><td>PolygonZkEVM</td><td>polygonzkevm</td><td>LeetSwap / leetswapzkevm</td></tr><tr><td>Loop</td><td>loop</td><td>Sphynx / sphynxloop<br>ZukeSwap / zukeswaploop</td></tr><tr><td>Kava</td><td>kava</td><td>Equilibre / equilibrekava<br>SurfSwap / surfswapkava</td></tr><tr><td>Metis</td><td>metis</td><td>Tethys / tethysmetis</td></tr><tr><td>Astar</td><td>astar</td><td>ArthSwap / arthswapastar<br>ZenLink / zenlinkastar</td></tr><tr><td>Oasis</td><td>oasis</td><td>YuzaSwap / yuzaswapoasis</td></tr><tr><td>IoTeX</td><td>iotex</td><td>Mimo / mimoiotex</td></tr><tr><td>Conflux</td><td>conflux</td><td>Swappi / swappiconflux</td></tr><tr><td>Canto</td><td>canto</td><td>LeetSwap / leetswapcanto</td></tr><tr><td>Energi</td><td>energi</td><td>EnergiSwap / energiswapenergi</td></tr><tr><td>Velas</td><td>velas</td><td>WagyuSwap / wagyuswapvelas</td></tr><tr><td>Grove</td><td>grove</td><td>GroveSwap / groveswapgrove</td></tr><tr><td>Pulse Chain</td><td>pulse</td><td>PulseX / pulsexpulse</td></tr><tr><td>BESC</td><td>besc</td><td>BeanSwap / beanswapbesc</td></tr><tr><td>Linea</td><td>linea</td><td>LeetSwap / leetswaplinea<br>HorizonDex / horizondexlinea</td></tr><tr><td>Base</td><td>base</td><td>LeetSwap / leetswapbase<br>RocketSwap / rocketswapbase<br>CBSwap / cbswapbase</td></tr><tr><td>Shibarium</td><td>shibarium</td><td>DogSwap / dogswapshibarium<br>MarSwap / marswapshibarium<br>LeetSwap / leetswapshibarium</td></tr><tr><td>opBNB</td><td>opbnb</td><td>CubiSwap / cubiswapopbnb<br>BinarySwap / binaryswapopbnb<br>LuigiSwap / luigiswapopbnb</td></tr><tr><td>Bitrock</td><td>bitrock</td><td>RockSwap / rockswapbitrock</td></tr><tr><td>Optimism</td><td>optimism</td><td>Uniswap V3 / uniswapv3optimism</td></tr><tr><td>Mantle</td><td>mantle</td><td>Agni /agnimantle<br>iZiSwap / iziswapmantle</td></tr><tr><td>LightLink</td><td>lightlink</td><td>Elektrik / elektriklightlink</td></tr><tr><td>Klaytn</td><td>klaytn</td><td>KlaySwap / klayswapklaytn</td></tr><tr><td>Solana</td><td>solana</td><td></td></tr><tr><td>Injective</td><td>injective</td><td></td></tr><tr><td>Radix</td><td>radix</td><td></td></tr><tr><td>Sui</td><td>sui</td><td></td></tr><tr><td>Manta Pacific</td><td>manta</td><td></td></tr><tr><td>ZetaChain</td><td>zeta</td><td>ZedaSwap / zedaswapzeta<br>MochaSwap / mochaswapzeta</td></tr></tbody></table>

_\*To add chains or DEXs, or for general support please reach out to the Quick Intel team in the_ [_Contact_](../../resources/support-and-team-contacts.md) _section._

### Integrations

With Quick Intel, we provided shareable links that can be shared with other users for ease of accessibility or direct link integrations.\
\
Below is an example of the format that should be followed to a direct link for scanning a token or an NFT.\
\
There are 3 parameters that the custom link should have.\
\- Type\
\- Chain\
\- Contract Address\
\
For "type" the available options are:\
\- token\
\- nft\
\
For "chain" the available options can be found in the [Chains](supported-chains-and-dex.md#chains) ID section above\
\
For "contractAddress" this will be the contract address of the token or NFT collection to be scanned.

[https://app.quickintel.io/scanner?type=token\&chain=arbitrum\&contractAddress=0x6d038130b9b379a373b1d33a29d5904ed1bb9026](https://app.quickintel.io/scanner?type=token\&chain=arbitrum\&contractAddress=0x6d038130b9b379a373b1d33a29d5904ed1bb9026)

### **LP Lock Providers**

Quick Intel supports the below LP lock providers for detection.

* UNCX
* Team Finance
* PinkSale
* GemPad
* OnlyMoons
* DxSale
* MaxxPloy
* IceCream Swap
* FatLocker
* SphynxLock
* Ceres

If there is a trusted and vetted LP Lock provider that you would like the Quick Intel team to support, please reach out to the team.\
\
\*_LP Burned currently only supports Uniswap V2 token based LP detectcions. We do not currently detect V3 LP Burns at the moment._
