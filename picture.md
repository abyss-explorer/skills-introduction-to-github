'''
graph LR
    A[物理信号<br/>电压/温度] --> B(下位机 MSP430);
    subgraph B
        direction LR
        B1[ADC模块] --> B2[MCU核心];
        B2 --> B3[UART模块];
    end
    B -- 串口通信 --> C(上位机 PC);
    subgraph C
        direction LR
        C1[UART接收] --> C2[数据解析];
        C2 --> C3[GUI显示];
    end
'''
