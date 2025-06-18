# 🌐 Geographic Routing Performance Testing Tool

A comprehensive browser-based tool for measuring and comparing network routing performance across different geographic paths and infrastructure providers.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/yourusername/geographic-routing-performance-tool)

## 🎯 What This Tool Does

The Geographic Routing Performance Testing Tool helps you optimize global network connectivity by:

- **Measuring latency** across different routing paths
- **Comparing performance** between traditional ISP routing vs optimized cloud backbone routing
- **Providing statistical analysis** with comprehensive performance metrics
- **Generating actionable insights** for infrastructure decisions

## ✨ Key Features

### 🎯 Flexible Testing Scenarios
- **Preset scenarios** for common routing optimizations (SA→AU→NZ, US→EU, Asia Pacific)
- **Custom scenario builder** for specific geographic requirements
- **Dynamic endpoint management** with route categorization
- **Visual route indicators** (Traditional, Optimized, Reference, Custom)

### 📊 Comprehensive Analysis
- **Statistical metrics**: average, median, min/max, standard deviation
- **Reliability tracking**: success rates and error analysis
- **Performance ranking** with automatic best/worst route identification
- **Improvement calculations** showing latency reduction and percentage gains

### 🛠️ Advanced Capabilities
- **Configurable test parameters**: iterations (10-100), timeout (5-30s)
- **Multiple test modes**: Latency-focused, Download tests, Comprehensive analysis
- **Real-time progress tracking** with per-endpoint status updates
- **CORS-aware testing** with clear feedback on blocked endpoints

### 📈 Rich Reporting
- **Interactive dashboards** with performance metrics
- **Detailed test logs** with timestamp tracking
- **Exportable results** in JSON format
- **Responsive design** for desktop, tablet, and mobile

## 🚀 Quick Start

### Option 1: Deploy to Vercel (Recommended)

1. Click the "Deploy with Vercel" button above
2. Connect your GitHub account
3. Deploy the project
4. Start testing your routes immediately

### Option 2: Local Development

```bash
# Clone the repository
git clone https://github.com/ces0491/network-latency-tester.git
cd network-latency-tester

# Install dependencies (optional - for local development server)
npm install

# Start local development server
npm run dev

# Or simply open index.html in your browser
```

### Option 3: Static Hosting

Simply upload the `index.html` and `docs.html` files to any static hosting provider (GitHub Pages, Netlify, AWS S3, etc.).

## 📖 Documentation

Visit the [complete documentation](docs.html) for:
- Detailed feature explanations
- Backend technology overview
- Usage examples and best practices
- Real-world application scenarios
- Technical considerations and limitations

## 🎯 Use Cases

### Infrastructure Decision Making
- **Cloud provider selection** based on actual performance data
- **CDN optimization** for global content delivery
- **Network architecture planning** with quantified impacts

### Development Workflow Optimization
- **Remote development environment** routing optimization
- **CI/CD pipeline** performance improvement
- **Database connection** latency reduction

### Business Case Development
- **Quantified performance improvements** for infrastructure investments
- **Cost-benefit analysis** with measurable latency reductions
- **ROI calculations** based on productivity improvements

## 🏆 Proven Results

**Case Study: SA→AU→NZ Development Team**
- **285ms latency reduction** (83% improvement)
- **5.9x faster response times** via Google Cloud backbone
- **Dramatic improvement in consistency** (±37ms vs ±145ms variation)

## 🛠️ Technical Details

### Browser-Based Architecture
- **No server required** - runs entirely in the browser
- **Modern JavaScript APIs** for high-precision timing
- **Client-side statistical analysis** and data processing
- **CORS-friendly** with automatic fallback handling

### Performance Measurement
```javascript
// High-precision timing using Performance API
const startTime = performance.now();
const response = await fetch(url, {
    method: 'HEAD',
    mode: 'cors',
    cache: 'no-cache'
});
const latency = performance.now() - startTime;
```

### Statistical Analysis
- Real-time calculations of comprehensive metrics
- Outlier detection and variance analysis
- Success rate tracking with detailed error categorization
- Performance trend analysis across multiple iterations

## 📊 Example Results

```json
{
  "bestRoute": {
    "name": "Google Cloud Australia",
    "average": 58,
    "min": 47,
    "max": 259,
    "standardDeviation": 37,
    "successRate": 100
  },
  "worstRoute": {
    "name": "Traditional Route (Europe)",
    "average": 343,
    "min": 307,
    "max": 1122,
    "standardDeviation": 145,
    "successRate": 100
  },
  "improvement": {
    "latencyReduction": 285,
    "percentageImprovement": 83
  }
}
```

## 🔧 Configuration Options

### Test Parameters
- **Iterations**: 10-100 (30 recommended for statistical significance)
- **Timeout**: 5-30 seconds (15 recommended for most scenarios)
- **Test Mode**: Latency (HEAD), Download (1KB), Comprehensive

### Route Types
- **Traditional**: Standard ISP routing
- **Optimized**: Cloud backbone or CDN routing
- **Reference**: Baseline or comparison endpoints
- **Custom**: User-defined routing paths

## ⚠️ Browser Compatibility

### Requirements
- Modern browsers with Fetch API and Performance API support
- Chrome 40+, Firefox 39+, Safari 10.1+, Edge 14+

### Limitations
- **CORS restrictions** may block some endpoints (alternatives provided)
- **Client-side measurements** may include browser overhead
- **Best for relative comparisons** rather than absolute latency measurements

### Development Setup
```bash
git clone https://github.com/yourusername/geographic-routing-performance-tool.git
cd geographic-routing-performance-tool
npm install
npm run dev
```
---