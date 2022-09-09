# vue3-chatbox-sample

This is a sample chatbox for Vue3. You can copy past requeired components.

![vue3-chatbox-sample](https://raw.githubusercontent.com/gislayer/vue3-chatbox-sample/main/src/assets/screen1.png)

### 1. ChatBox.vue Main Component
This is main vue component for ChatBox. It has providers and methods

#### 1.1. ChatHeader.vue Component
This is sub component for ChatBox.vue File. Injected title prop info coming from ChatBox.vue providers.

#### 1.2. ChatBody.vue Component
This component created for showing user and robot messages. Injected chatData object info comming from ChatBox.vue providers.

##### 1.2.1 ChatMessage.vue Component
This component created for showing message items. Injected chatData object info comming from ChatBox.vue providers.

#### 1.2. ChatAction.vue Component
This component created for adding new user message. Injected 'addMessage', 'users', 'sender' providers. it's defined at ChatBox.vue file.

## Installing
	npm install
	yarn install
## Run
	npm run serve
	yarn serve