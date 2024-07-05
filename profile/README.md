# CAPSTONE-DIDI

## ✅ DIDI

# 목차
1. [DIDI?](#didi)
2. [기획배경 및 목적](#기획배경-및-목적)
3. [Installation & Development](#installation--development)
4. [PPT](#ppt)
5. [Demo](#demo)

## DIDI?
DIDI는 [DID(decentralized identity, 탈중앙화 신원증명)](https://www.w3.org/TR/did-core/) 와 [VC(verifiable credential,검증가능한 신원)](https://www.w3.org/TR/vc-data-model-2.0/)을 이용한 블록체인 투표시스템입니다.  

## 기획배경 및 목적

## VC/VP를 이용한 투표 과정
### VC방식✅

- 회원가입이 완료된 회원은 VC(이름, 이메일)을 제공 받는다.
- 투표방 생성시 유권자들의 정보(이름, 이메일)를 기입
    - DB에 단방향 암호화한 유권자들의 정보(이름,이메일)하고 투표방번호를저장
- 유권자들의 이메일로 (해당 투표방의  투표권에 해당하는) VC제공을 위한 connection요청 메일을 보낸다.
- 유권자가 해당 connection요청을 승락 시 해당 투표방에 대한 VP검증(이름, 이메일)
    - DB에서 찾아서 존재한다면 해당투표방의 유권자가 확인됨
- 검증성공 시 (해당 투표방의 투표권에 해당하는) VC를 추가 제공
- 이후 유권자가 투표하기위해 투표방에 접속 시 VP로 투표권만 제공
- 해당 투표방에 대한 VP가 맞을 시 투표방에 접속가능

```
0. 링크가 다른 사용자에게 제공 또는 탈취됨을 막기위해 해당 링크에 접속한 사용자에 대한 VP(이름,이메일)검증
	을 통해 DB에 저장된 유권자가 맞는지 확인.

1. 투표권 VP 검증 과정에 (1)VC발급자를 확인하는 과정과 (2)값을 확인 과정이 수반되므로 투표권 위변조 해결가능

2. 투표방 생성시 제공되는 이메일의 중복 여부만 검사한다면 이메일당 하나의 투표권만 제공되므로 중복투표 해결가능

3. VP검증만 완료된다면 투표방에 접근가능. 투표방 접근이후에는 사용자 정보가 기록되지 않으므로 비밀 투표 해결가능
```

단, 유권자들은 미리 개별링크 접속전 회원가입이 이루어져야 한다.

## 시스템구성도 (투표시스템은 구성도는 아직 완성x)

<img width="918" alt="image" src="https://github.com/CAPSTONE-DIDI/.github/assets/92563695/781f875d-3445-4aa7-af20-8811560ed945">

## Installation & Development

## PPT

## Demo

## 참고
