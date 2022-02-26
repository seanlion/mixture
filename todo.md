## 해야될 것

### 요구사항
- 시약을 Mint 할 수 있어야 한다.
- 시약 2개를 가지고 혼합물 NFT를 Mint할 수 있어야 한다.(Mint는 비용이 든다.)
    - 시약의 authority를 우리 프로그램 소유로 한다.
- 혼합물 NFT는 시약 2개를 자식으로 가져야 한다.

- Mint한 시약을 UI에서 볼 수 있어야 한다. => FE에서 처리 가능
- 선택한 input들이 혼합물 NFT의 자식과 일치하는지 체크할 수 있어야 한다.(대조 기능) => FE에서 처리 가능


### 시약 Mint
Mint요청(UI) -> 메타플렉스 // TS 이용
### 혼합물 Mint
instruction : 
  0.프로그램 initialize (account initialize/deinitialize)
    - data account 만들기

  1.owner의 authority를 mixture로 setup(transferBetweenAccounts)
  2.mintNFT(children의 addresses, candyMachine에 보낼 accounts)
  
### 해야할 것
프론트에서 어떻게 remaining accounts를 넘길거냐 // https://solanacookbook.com/guides/serialization.html#serializing-instruction-data
받은 accounts를 캔디머신 코드에서 어떻게 분기처리할거냐?

