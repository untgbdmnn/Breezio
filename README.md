# Breezio 🌤️

A modern, responsive weather dashboard application built with React, TypeScript, and Tailwind CSS. Breezio provides real-time weather information for any location worldwide, featuring beautiful data visualizations, dark/light theme support, and seamless user experience.

---

## 🚀 Features

### **Real-Time Weather Tracking**
- **Current Weather Conditions**: Display temperature, feels like, humidity, wind speed, pressure, and visibility
- **Hourly Temperature Forecast**: Interactive hourly temperature chart showing 24-hour trends
- **5-Day Weather Forecast**: Comprehensive daily forecasts with weather conditions and temperature ranges
- **Geolocation Support**: Automatically detect user's location for local weather updates
- **City Search**: Search and browse weather for any city worldwide using OpenWeatherMap API

### **City Management**
- **Favorite Cities**: Save and manage favorite cities for quick access
- **Persistent Storage**: Favorites are stored locally using browser local storage
- **Quick Navigation**: Easy access to favorite cities from the dashboard

### **User Experience**
- **Dark/Light Theme**: Seamless dark/light mode switching with system preference detection
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Loading States**: Beautiful skeleton loading animations while fetching data
- **Error Handling**: Comprehensive error messages with retry functionality
- **Toast Notifications**: User feedback for successful actions

### **Data Visualization**
- **Interactive Charts**: Hourly temperature visualization using Recharts
- **Weather Icons**: Visual representations of weather conditions (clear sky, rain, clouds, etc.)
- **Clean UI**: Modern, intuitive interface built with shadcn/ui components

---

## 🛠️ Technologies Used

### **Core Technologies**
- **React 18.3**: Modern UI library with functional components and hooks
- **TypeScript 5.6**: Type-safe JavaScript for better development experience
- **Vite 5.4**: Fast build tool and development server
- **ESLint**: Code quality and consistency

### **Styling & UI**
- **Tailwind CSS 3.4**: Utility-first CSS framework
- **shadcn/ui**: Beautiful, accessible UI components built with Radix UI
- **Tailwind CSS Animate**: Animation utilities for Tailwind
- **Lucide React**: Beautiful and consistent icon set

### **State Management & Data Fetching**
- **TanStack React Query 5**: Powerful data fetching and caching library
- **TanStack React Query Devtools**: Development tools for debugging
- **React Router DOM 6**: Client-side routing

### **Utilities & Helpers**
- **date-fns 4.1**: Modern JavaScript date utility library
- **Recharts 2.13**: Composable charting library for React
- **Class Variance Authority (CVA)**: Component variant management
- **clsx & tailwind-merge**: Conditional className utilities
- **next-themes 0.4**: Theme handling for Next.js and React
- **Sonner 1.7**: Beautiful, accessible toast notifications

### **Development Tools**
- **TypeScript ESLint**: TypeScript-aware linting
- **PostCSS**: CSS transformation
- **Autoprefixer**: Automatic vendor prefixes
- **@types/node**: Node.js type definitions

---

## 📦 Installation

### **Prerequisites**
- Node.js 18+ 
- npm or yarn package manager
- OpenWeatherMap API key (free tier available)

### **Setup Instructions**

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd breezio
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Create environment file**
   ```bash
   cp .env.example .env
   ```

4. **Add your OpenWeatherMap API key**
   ```env
   VITE_OPENWEHATHER_API_KEY=your_api_key_here
   ```

5. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

6. **Open your browser**
   Navigate to `http://localhost:3000`

---

## 🔧 Available Scripts

- `npm run dev` - Start development server on port 3000
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

---

## 📁 Project Structure

```
breezio/
├── public/                 # Static assets
├── src/
│   ├── components/        # React components
│   │   ├── ui/           # shadcn/ui components
│   │   ├── currentWeather.tsx
│   │   ├── favorite-button.tsx
│   │   ├── favorite-city.tsx
│   │   ├── header.tsx
│   │   ├── hourly-tem.tsx
│   │   ├── layout.tsx
│   │   ├── weather-details.tsx
│   │   └── weather-forecast.tsx
│   ├── hooks/            # Custom React hooks
│   │   ├── use-favorite.ts
│   │   ├── use-geolocation.ts
│   │   ├── use-local-storage.ts
│   │   ├── use-search-history.ts
│   │   └── use-weather.ts
│   ├── helper/           # Utility functions and types
│   │   ├── api.ts
│   │   ├── type.ts
│   │   └── weather.ts
│   ├── constants/        # Constant values
│   │   └── theme-provider.tsx
│   ├── pages/            # Page components
│   │   ├── city-list.tsx
│   │   └── weather-dashboard.tsx
│   ├── lib/              # Library utilities
│   │   └── utils.ts
│   ├── App.tsx          # Main application component
│   ├── main.tsx         # Application entry point
│   └── index.css        # Global styles
├── .env.example         # Environment variables template
├── .gitignore
├── eslint.config.js
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

---

## 🌐 API Reference

Breezio uses the **OpenWeatherMap API** for weather data:

### **Endpoints Used**
- **Current Weather**: `GET /weather`
- **Forecast**: `GET /forecast`
- **Geocoding**: `GET /direct` and `GET /reverse`

### **Parameters**
- `lat`: Latitude
- `lon`: Longitude
- `appid`: API key
- `units`: Temperature unit (metric)
- `lang`: Language

---

## 🎨 Design System

### **Color Palette**
- **Primary**: Modern blue tones for trust and reliability
- **Accents**: Subtle gradients and shadows
- **Dark Mode**: Deep, comfortable dark colors
- **Light Mode**: Clean, crisp light colors

### **Components**
All UI components are built using **shadcn/ui** with Tailwind CSS, ensuring:
- Full accessibility (WCAG 2.1 compliant)
- Dark mode support
- Keyboard navigation
- Screen reader compatibility

---

## 📱 Responsive Design

Breezio is fully responsive and works seamlessly across:
- 🖥️ Desktop (1200px+)
- 💻 Laptop (992px - 1199px)
- 📱 Tablet (768px - 991px)
- 📱 Mobile (< 768px)

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```env
VITE_OPENWEHATHER_API_KEY=your_openweathermap_api_key
```

Get your free API key at: [OpenWeatherMap](https://openweathermap.org/api)

---

## 🚀 Deployment

### **Build for Production**
```bash
npm run build
```

The built files will be in the `dist/` directory.

### **Deploy to Vercel/Netlify**
1. Push your code to GitHub
2. Connect your repository to Vercel or Netlify
3. Add environment variables in the deployment settings
4. Deploy!

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgments

- [OpenWeatherMap](https://openweathermap.org/) for providing the weather data API
- [shadcn](https://ui.shadcn.com/) for the beautiful UI components
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [TanStack Query](https://tanstack.com/query) for excellent data fetching utilities

---

## 📣 Hashtags

#WeatherApp #React #TypeScript #TailwindCSS #OpenWeatherMap #TanStackQuery #ResponsiveDesign #DarkMode #RealTimeWeather #WebDevelopment #Frontend #Dashboard #JavaScript #Vite #HookBased #ModernUI #Accessibility #DataVisualization #WeatherForecast #APIIntegration #ComponentLibrary #CleanCode #DeveloperTools #OSS #OpenSource #Coding #Programming #Tech

---

**Built with ❤️ using React, TypeScript, and modern web technologies.**

