# StockFlow - Real-Time Stock Signal Analysis Microservice

StockFlow is an automated stock analysis platform developed to enhance the efficiency of identifying potential trading opportunities. Designed to replicate and automate the analytical methods and indicators I typically employ, StockFlow systematically evaluates a broad range of stocks and generates a curated shortlist of candidates warranting further review.

## Why was it built ?
This tool is intended to serve as an initial screening layer for me, providing structured assistance in narrowing down the universe of stocks to those with promising characteristics. It is not a definitive prediction system to be relied upon blindly but rather a time-saving aid that supports more focused and informed decision-making. By automating the preliminary stages of analysis, StockFlow significantly reduces the effort and time required by me to identify high-potential stocks for further evaluation.

## Who is it for ?
Anyone who wants to trim down potential stocks to a limited count so that they can invest less time in initial screening and focus on more deeper analysis.

## Features

### **Signal Engine**
- **Multi-Indicator Analysis**: Identifying potential entry points by combining signals from RSI, MACD, Bollinger Bands, CMF (Chaikin Money Flow)
- **Real-time Data**: Live stock data from Yahoo Finance
- **Confidence Scoring**: Signal strength assessment (Weak/Strong)

### **Technical Indicators**
- **RSI (Relative Strength Index)**: Momentum oscillator with smoothing
- **MACD (Moving Average Convergence Divergence)**: Trend and momentum analysis
- **Bollinger Bands**: Volatility and price channel analysis
- **CMF (Chaikin Money Flow)**: Volume-weighted price analysis

### **API Services**
- **Signal Engine API**: Real-time stock analysis endpoints
- **Controller API**: Administrative and cronjob management
- **CORS Support**: Cross-origin request handling
- **Error Handling**: Comprehensive error responses
- **Authentication for selected APIs**: API Key Authentication for administrative and sensitive endpoints 

### **Automation & Monitoring**
- **Scheduled Analysis**: Automated cronjobs for regular stock screening
- **Email Notifications**: Email alert with potential stocks during scheduled analysis
- **Health Monitoring**: Automated system health check and status monitoring with email alert on failure

### **Deployment & Infrastructure**
- **Lightweight Kubernetes**: Full K3s deployment with Role based access control
- **Docker Containerization**: Microservice architecture
- **Traefik Ingress**: Provides routing with TLS encryption using Traefik, and configures CORS to allow cross-service API calls securely.
- **ConfigMaps & Secrets**: Secure configuration management with kubernetes secrets and configmaps
- **CI/CD Pipeline with Automated Deployment**: Automated deployment using Github Actions to k3s cluster
- **Cloud VM for complete deployment**: The entire service runs on Oracle Cloud Infrastructure VM which acts as a self hosted runner as well, on Github Actions.
- **Static Frontend**: Static Frontend for stockflow APIs using Bootstrap, CSS, Javascript.
