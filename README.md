# The Cube - Mediation Device

**Course:** Software Systems
**Status:** In Development


## Features 
- **Press to Meditate**
- **Webapp Control of Cube**
- **Customizable Colors**
- **Customizable Breathing Paterns**
- **Customizable Times**
- **Meditation Tracking**
- 
-
-


```mermaid 
graph TD
    User1((User)) -- Button Press--> ESP[ESP32 System]
    User1((User)) --> W_APP[Web APP]
    
    ESP <--> DB[(Database)] 
    W_APP <-->DB
    ESP <--> W_APP

```

```mermaid 
graph LR
    subgraph Hardware
        P[Piezo-electric button] -- Analog --> ADC[ADC]
        ADC --> ESP[ESP32]
        ESP -- I2C --> LED_D[LED Driver]
        LED_D --> RGBW[RGBW LED]
    end

    subgraph Software
        W_APP_CLIENT[Client/Gui]
        W_APP_SERVER[Server]
        DB[(Database)]
        


    end

 
    %% Communication Flows
    W_APP_CLIENT <--> W_APP_SERVER
    ESP <--> W_APP_SERVER
    W_APP_SERVER <--> DB
```

## About
This is application/product project for a meditation cube.
- Modular Design
- Network Communication
- Security Fundamentals


**Team Members:**
1. Parry Zhuo
2. Sasha Roosen-Saba
3. Bryce Reid
4. Kale Wyse
