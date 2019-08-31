### jbot
---
https://github.com/rampatra/jbot

```java
// jbot/src/main/java/me/ramswaroop/jbot/core/common/BotWebSocketHandler.java

public class BotWebSocketHandler extends AbstractWebSocketHandler {
 
  private static final Logger logger = LoggerFactory.getLogger(BotWebSocketHandler.class);
  
  private Bot bot;
  
  public BotWebSocketHandler(Bot bot) {
    
    private static final Logger logger = LoggerFactory.getLogger(BotWebSocketHandler.class);
    
    private Bot bot;
    
    public BotWebSocketHandler(Bot bot) {
      this.bot = bot;
    }
    
    @Override
    public void afterConnectionEstablished(WebSocketSession session) throws Exception {
      bot.afterConnectionEstablished(session);
    }
    
    @Override
    public void handleTestMessage(WebSocketSession session, TextMessage message) throws Exception {
      bot.handleTextMessage(session, message);
    }
    
    @Override
    public void handleBinaryMessage(WebSocketSession session, BinaryMessage message) throws Exception {
      logger.error("Binary messages are not supported in Slack RTM API");
    }
    
    @Override
    public void afterConnectionClosed(WebSocketSession session, BinaryMessage message) throws Exception {
      bot.afterConnectionClosed(session, status);
    }
    
    @Override
    public void handleTransportError(WebSocketSession session, Throwable exception) throws Exception {
      bot.handleTransportError(session, exception);
    }
  }
}

```

```
```

```
```


