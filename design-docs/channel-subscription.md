# channel-subscription

## description

After subscribing to a channel, the channel is still retained after exiting the application, instead of automatically deleting it except for the default channel. You can see this channel again in the channel list the next time you open the application. After canceling the subscription, after closing the application, the channels other than the default channel will be automatically deleted. The next time you open the application, you will not be able to see this channel in the channel list. You need to search for the channel again to join the channel.

## why design

- It is convenient for users to quickly find and enter the channel they want to enter, instead of searching the channel again and joining. Improve user experience.