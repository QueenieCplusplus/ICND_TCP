# ICND TCP
Transmission Control Protocol (end-to-end)

傳輸控制協定定義了端點對端點 Host - to Host 兩主機設備（非網路設備）的連線程序。


# TCP/IP

        +---------+-----------+
        | Network | Transport |
        +---------+-----------+
        |         |    TCP    |
        |    IP   +===========+
        |         |    UDP    |
        +---------+-----------+
        |   IPX   |    SPX    |
        +---------+-----------+

# App Id & SAP

利用 port 辨識出上層應用程式辨識器 app id，使得各端點 end point 能夠組合分解來自更上層 (L5、 L6、L7) 的資料段 chunck or segement，將其轉換為本層需要的資料流。

關於此 port 為 SAP 服務存取端點，此乃與 L2 的 SAP 不同。

# Connection-Oriented

藉由系統間的連結導向，保證的效果：

- [x] 確保了資料段傳送的結果會傳回確認通知發送端。

- [x] 擁有 retransmission 功能，確保了資料段送出卻無收回回應時。

- [x] 接收端能將資料段按照正確的順序組合。

- [x] 避免線路壅塞。

# UDP

如通訊電話軟體，為了確保速度和使用者體驗，不會使用連結導向來保證訊息即時收到確認通知。

