<template>
	<view class="emoji">
		<view class="emoji_row" v-for="(item,index) in emoji" :key="index">
			<view class="emoji_item" v-for="(v,i) in item" :key="i" @tap="emojiTap(v)">{{v}}</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				emoji:[
					['😀','😁','😂','🤣','😄','😅','😆','😉'],
					['😊','😋','😎','😍','😘','😗','😙','😚'],
					['🙂','🤗','🤔','😐','😑','😶','🙄','😏'],
					['😣','😥','😮','🤐','😯','😪','😫','😴'],
					['😌','😛','😜','😝','🤤','😒','😓','😕'],
					['🙃','🤑','😲','🙁','😖','😞','😤','😭'],
					['😨','😩','😬','😰','😱','😳','😵','😡'],
					['😠','😷','🤒','🤕','🤢','🤧','😇','🤠'],
					['🤡','🤥','🤓','😈','👿','👹','👹','💀'],
					['👻','💩','😺','😻','😹','😼','😽','🙀'],
					['😿','😾','🗣','👤','👥','👫','👭','👂'],
					['👃','👣','👀','👁','👅','👄','👓','👔'],
					['👕','👖','👗','👘','👙','👞','👢','👠'],
					['👒','👑','💄','💍','⛑','🌂','💼','🎓']
				]
			}
		},
		methods: {
			emojiTap(v){
				this.$emit('getEmoji',v)
			}
		}
	}
</script>

<style lang="scss">
.emoji{
	width: 100%;
	height: 460rpx;
	padding:16rpx 12rpx 95rpx ;
	overflow: hidden;
	overflow-y: auto;
	.emoji_row{
		display: flex;
		
		.emoji_item{
			flex: 1;
			display: flex;
			justify-content: center;
			align-items: center;
			font-size: 40rpx;
			line-height: 80rpx;
		}
	}
}
</style>
