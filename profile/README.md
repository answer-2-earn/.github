![Cover](/profile/cover.png)

# ❓ Answer 2 Earn

Answer fan questions, earn LYX rewards — a LUKSO Mini-App with AI verification.

## ✨ Background

In the past, personal question and answer apps have been popular and viral. The largest one, ask.fm, had 50 million monthly active users. With the capabilities of Lukso and AI, this idea can be improved and achieve greater performance.

## 🛠️ How it works

The Mini-App facilitates a question-and-answer interaction between users (Askers and Answerers) on the LUKSO Mainnet, leveraging Universal Profiles and smart contracts.

- **Asking a Question (Asker)**

  - The Asker navigates to the Answerer's profile on Universal Everything.
  - Connects their Universal Profile to the Mini-App using `@up-provider`.
  - Submits a question including text and a LYX reward.
  - The backend generates LSP8 token metadata for the question using `erc725.js` and uploads it to Pinata IPFS.
  - An LSP8 token representing the question is minted via the `QuestionManager` and `Question` smart contracts on the LUKSO Mainnet.

- **Answering a Question (Answerer)**

  - The Answerer accesses the Mini-App through their Universal Profile.
  - Connects their Universal Profile using `@up-provider`.
  - Views a list of unanswered questions, sortable by reward amount.
  - Selects and submits an answer to a chosen question.
  - An AI service (Gemini 2.5 Flash) verifies if the answer is relevant to the question.
  - If the answer is valid, the `QuestionManager` smart contract transfers the specified LYX reward to the Answerer's Universal Profile.

## 🔗 Artifacts

- Application - https://answer-2-earn.vercel.app/
- Demo - https://universaleverything.io/0x4018737e0D777b3d4C72B411a3BeEC286Ec5F5eF?assetGroup=grid
- Contracts (LUKSO Mainnet):
  - Question - https://explorer.execution.mainnet.lukso.network/address/0x67e3648A46f970f91D2989643bF8479b76795Bb2
  - Question Manager - https://explorer.execution.mainnet.lukso.network/address/0xe9b3E53Cd4f92DE36aF02e9B763c3Fe5eb02ee0C

## 🛠️ Technologies

- LSP8 standard is used for a contract that stores questions and sends rewards for answers.
- LUKSO Mainnet is used as a blockchain for development and beta testing.
- Universal Profiles is used to make the app more social by displaying profile pictures and usernames.
- @up-provider is used as a tool to integrate the app with the LUKSO grid.
- erc725.js library is used to encode and decode profile and question metadata.
- Pinata IPFS is used to store metadata with questions and answers.
- Gemini AI is used to verify that answers match questions.

## 🏗️ Architecture

![Architecture](/profile/architecture.png)
