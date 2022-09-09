# vue3-chatbox-sample

This is a sample chatbox for Vue3. You can copy past requeired components.

![vue3-chatbox-sample](https://i.ibb.co/r58vhNZ/screen1.png)

### 1. ChatBox.vue Main Component
This is main vue component for ChatBox. It has providers and methods

#### 1.1. ChatHeader.vue Component
This is sub component for ChatBox.vue File. Injected title prop info coming from ChatBox.vue providers.

#### 1.2. ChatAction.vue Component
This component created for adding new user message. Injected 'addMessage', 'users', 'sender' providers. it's defined at ChatBox.vue file.

#### 1.3. ChatBody.vue Component
This component created for showing user and robot messages. Injected chatData object info comming from ChatBox.vue providers.

##### 1.3.1 ChatMessage.vue Component
This component created for showing message items. Injected chatData object info comming from ChatBox.vue providers.

## Installing
	npm install
	yarn install
## Run
	npm run serve
	yarn serve