```js
const { AvatarSize } = require('../../components/Avatar');
const { FixedGridRow, FixedGridColumn } = require('../../components/FixedGrid');
const { GutterSize } = require('../../components/Block');
const { TextColor, TextSize } = require('../../components/Text');


const user1 = {
  image: 'user.png',
  name: 'Sally Super-super-super-long-middle-name Smilefields',
};
const user2 = {
  image: 'user.png',
  name: 'Tiny Tim',
};

<FixedGridRow gutterSize={GutterSize.LARGE}>
  <FixedGridColumn fixed={true} width={32}>
    <Avatar imageUrl={user1.image} name={user1.name} size={AvatarSize.SMALL} />
  </FixedGridColumn>
  <FixedGridColumn>
    <Block bottomSpacing={GutterSize.XSMALL} className="byline">
      <Text maxWidth="100%">
        <Text bold={true}>{user1.name}</Text> <Text color={TextColor.METADATA} size={TextSize.MEDIUM_SUB}>in reply to</Text> <Text bold={true}>{user2.name}</Text>
      </Text> <Text color={TextColor.METADATA} size={TextSize.MEDIUM_SUB}> - 5 hours ago from Desktop</Text>
    </Block>
    <Block bottomSpacing={GutterSize.MEDIUM} className="message">
      hey that's a great idea! let's discuss this further at the monthly offsite next week
    </Block>
    <Block textSize={TextSize.SMALL} className="actions">
      <HorizontalList>
        <HorizontalListItem>
          <Clickable><Icon icon="like" /> Like</Clickable>
        </HorizontalListItem>
        <HorizontalListItem>
          <Clickable><Icon icon="edit" /> Reply</Clickable>
        </HorizontalListItem>
        <HorizontalListItem>
          <Clickable><Icon icon="share" /> Share</Clickable>
        </HorizontalListItem>
        <HorizontalListItem>
          <Clickable>...</Clickable>
        </HorizontalListItem>
      </HorizontalList>
    </Block>
  </FixedGridColumn>
</FixedGridRow>
```
