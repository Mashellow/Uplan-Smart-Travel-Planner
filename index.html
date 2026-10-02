<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UPlan - Smart Travel Planner & Itinerary System</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- React 18 & ReactDOM 18 CDN -->
  <script src="https://unpkg.com/react@18/umd/react.production.min.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js" crossorigin></script>
  
  <!-- Babel Standalone CDN -->
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  
  <!-- Google Fonts: Prompt -->
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600;700;800&display=swap');
    body {
      font-family: 'Prompt', sans-serif;
    }
    /* Hide scrollbars for clean UI */
    .no-scrollbar::-webkit-scrollbar {
      display: none;
    }
    .no-scrollbar {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }
  </style>
</head>
<body class="bg-[#F8FAFC] text-slate-800 antialiased selection:bg-blue-500 selection:text-white">

  <!-- Root Container for React -->
  <div id="root"></div>

  <!-- React Application Logic -->
  <script type="text/babel">
    const { useState, useEffect } = React;

    // --- DATA CONSTANTS ---
    const PROVINCES_DATA = [
      { id: 'all', name: 'ทุกจังหวัด (All Thailand)', icon: '🇹🇭' },
      { id: 'bangkok', name: 'กรุงเทพมหานคร (Bangkok)', icon: '🏙️' },
      { id: 'chiangmai', name: 'เชียงใหม่ (Chiang Mai)', icon: '⛰️' },
      { id: 'phuket', name: 'ภูเก็ต (Phuket)', icon: '🏖️' },
      { id: 'krabi', name: 'กระบี่ (Krabi)', icon: '🏝️' },
      { id: 'pattaya', name: 'ชลบุรี / พัทยา (Pattaya)', icon: '⛵' },
    ];

    const MACRO_PINS = [
      {
        id: 'm-bkk',
        provinceId: 'bangkok',
        name: 'กรุงเทพมหานคร',
        enName: 'Bangkok',
        placesCount: 154,
        coords: { top: '48%', left: '46%' },
        image: 'https://images.unsplash.com/photo-1508009603885-50cf7c579365?auto=format&fit=crop&w=500&q=80',
        icon: '🏙️',
        avgBudget: '15,000 - 35,000 ฿'
      },
      {
        id: 'm-cnx',
        provinceId: 'chiangmai',
        name: 'เชียงใหม่',
        enName: 'Chiang Mai',
        placesCount: 128,
        coords: { top: '22%', left: '28%' },
        image: 'https://images.unsplash.com/photo-1512553353614-82a7370096dc?auto=format&fit=crop&w=500&q=80',
        icon: '⛰️️',
        avgBudget: '12,000 - 28,000 ฿'
      },
      {
        id: 'm-hkt',
        provinceId: 'phuket',
        name: 'ภูเก็ต',
        enName: 'Phuket',
        placesCount: 96,
        coords: { top: '78%', left: '32%' },
        image: 'https://images.unsplash.com/photo-1589394815804-964ed0be2eb5?auto=format&fit=crop&w=500&q=80',
        icon: '🏖️',
        avgBudget: '18,000 - 45,000 ฿'
      },
      {
        id: 'm-kbv',
        provinceId: 'krabi',
        name: 'กระบี่',
        enName: 'Krabi',
        placesCount: 82,
        coords: { top: '74%', left: '38%' },
        image: 'https://images.unsplash.com/photo-1552465011-b4e21bf6e79a?auto=format&fit=crop&w=500&q=80',
        icon: '🏝️',
        avgBudget: '15,000 - 32,000 ฿'
      },
      {
        id: 'm-pty',
        provinceId: 'pattaya',
        name: 'ชลบุรี / พัทยา',
        enName: 'Pattaya / Chonburi',
        placesCount: 110,
        coords: { top: '54%', left: '56%' },
        image: 'https://images.unsplash.com/photo-1528181304800-259b08848526?auto=format&fit=crop&w=500&q=80',
        icon: '⛵',
        avgBudget: '10,000 - 25,000 ฿'
      }
    ];

    const LOCAL_PLACES = [
      {
        id: 'p-1',
        provinceId: 'bangkok',
        name: 'วัดอรุณราชวราราม ราชวรมหาวิหาร',
        category: 'Attraction',
        categoryName: 'สถานที่ท่องเที่ยว',
        price: '100 ฿',
        priceNum: 100,
        rating: 4.9,
        reviews: 2450,
        coords: { top: '44%', left: '46%' },
        image: 'https://images.unsplash.com/photo-1563492065599-3520f775eeed?auto=format&fit=crop&w=600&q=80',
        subtext: 'วัดโบราณริมแม่น้ำเจ้าพระยา พระปรางค์โดดเด่นงามสง่า เอกลักษณ์สถาปัตยกรรมไทย',
        tag: 'แลนด์มาร์กยอดนิยม'
      },
      {
        id: 'p-2',
        provinceId: 'bangkok',
        name: 'วัดพระศรีรัตนศาสดาราม (วัดพระแก้ว)',
        category: 'Attraction',
        categoryName: 'สถานที่ท่องเที่ยว',
        price: '500 ฿',
        priceNum: 500,
        rating: 4.9,
        reviews: 3120,
        coords: { top: '40%', left: '42%' },
        image: 'https://images.unsplash.com/photo-1508009603885-50cf7c579365?auto=format&fit=crop&w=600&q=80',
        subtext: 'วัดคู่บ้านคู่เมืองกรุงเทพฯ ประดิษฐานพระพุทธมหามณีรัตนปฏิมากร งดงามสมพระเกียรติ',
        tag: 'มรดกวัฒนธรรม'
      },
      {
        id: 'p-3',
        provinceId: 'chiangmai',
        name: 'คาเฟ่ลายท่า เชียงใหม่ (Lai Tha Cafe)',
        category: 'Cafe',
        categoryName: 'คาเฟ่ & ร้านอาหาร',
        price: '120 ฿',
        priceNum: 120,
        rating: 4.8,
        reviews: 890,
        coords: { top: '22%', left: '26%' },
        image: 'https://images.unsplash.com/photo-1554118811-1e0d58224f24?auto=format&fit=crop&w=600&q=80',
        subtext: 'คาเฟ่บรรยากาศสโลว์ไลฟ์ กลางเมืองเก่าเชียงใหม่ กาแฟดีเยี่ยม มุมถ่ายรูปเพียบ',
        tag: 'สายถ่ายรูป'
      },
      {
        id: 'p-4',
        provinceId: 'chiangmai',
        name: 'ถนนคนเดินท่าแพ',
        category: 'Souvenir',
        categoryName: 'ของฝาก & ช้อปปิ้ง',
        price: 'ฟรี',
        priceNum: 0,
        rating: 4.7,
        reviews: 1850,
        coords: { top: '26%', left: '30%' },
        image: 'https://images.unsplash.com/photo-1533105079780-92b9be482077?auto=format&fit=crop&w=600&q=80',
        subtext: 'ตลาดนัดถนนคนเดินยอดฮิต ช้อปของฝาก งานคราฟต์ และอาหารพื้นเมืองเชียงใหม่',
        tag: 'สตรีทฟู้ด & ของฝาก'
      },
      {
        id: 'p-5',
        provinceId: 'phuket',
        name: 'แหลมพรหมเทพ ภูเก็ต',
        category: 'Attraction',
        categoryName: 'สถานที่ท่องเที่ยว',
        price: 'ฟรี',
        priceNum: 0,
        rating: 4.8,
        reviews: 3400,
        coords: { top: '78%', left: '30%' },
        image: 'https://images.unsplash.com/photo-1589394815804-964ed0be2eb5?auto=format&fit=crop&w=600&q=80',
        subtext: 'จุดชมวิวพระอาทิตย์ตกดินที่สวยที่สุดในประเทศไทย มองเห็นทะเลอันดามันสุดสายตา',
        tag: 'จุดชมวิวสุดปัง'
      },
      {
        id: 'p-6',
        provinceId: 'bangkok',
        name: 'โรงแรมศาลา อรุณ (Sala Arun)',
        category: 'Stay',
        categoryName: 'ที่พักแนะนำ',
        price: '3,800 ฿',
        priceNum: 3800,
        rating: 4.8,
        reviews: 430,
        coords: { top: '46%', left: '50%' },
        image: 'https://images.unsplash.com/photo-1566073771259-6a8506099945?auto=format&fit=crop&w=600&q=80',
        subtext: 'โรงแรมบูทีควิววัดอรุณ ติดริมแม่น้ำเจ้าพระยา บรรยากาศโรแมนติกยามค่ำคืน',
        tag: 'ที่พักวิวหลักล้าน'
      },
      {
        id: 'p-7',
        provinceId: 'krabi',
        name: 'อ่าวไร่เลย์ กระบี่ (Railay Beach)',
        category: 'Attraction',
        categoryName: 'สถานที่ท่องเที่ยว',
        price: 'ฟรี',
        priceNum: 0,
        rating: 4.9,
        reviews: 1920,
        coords: { top: '72%', left: '38%' },
        image: 'https://images.unsplash.com/photo-1552465011-b4e21bf6e79a?auto=format&fit=crop&w=600&q=80',
        subtext: 'ชายหาดสวยระดับโลก ล้อมรอบด้วยผาหินปูนสูงเสียดฟ้า เหมาะแก่การปีนผาและเล่นน้ำ',
        tag: 'ธรรมชาติสุดอลัง'
      },
      {
        id: 'p-8',
        provinceId: 'pattaya',
        name: 'ปราสาทสัจธรรม พัทยา',
        category: 'Attraction',
        categoryName: 'สถานที่ท่องเที่ยว',
        price: '500 ฿',
        priceNum: 500,
        rating: 4.7,
        reviews: 1610,
        coords: { top: '52%', left: '60%' },
        image: 'https://images.unsplash.com/photo-1528181304800-259b08848526?auto=format&fit=crop&w=600&q=80',
        subtext: 'ปราสาทไม้แกะสลักริมทะเลที่ใหญ่ที่สุดในโลก งานประณีตทรงคุณค่าเชิงสถาปัตย์',
        tag: 'ไฮไลต์พัทยา'
      }
    ];

    const INITIAL_DAYS_DATA = [
      {
        id: 'day1',
        label: 'DAY 1',
        dateStr: '10 พ.ย. 2026',
        title: 'วันแรก: เช็กอินเมืองเก่า & ชมวัดอรุณริมแม่น้ำ',
        totalDist: '12.4 กม.',
        totalTime: '45 นาที',
        transportMode: '🚗 รถยนต์ส่วนตัว / แท็กซี่',
        activities: [
          {
            id: 'a-1',
            time: '09:00 - 11:30',
            title: 'วัดพระศรีรัตนศาสดาราม (วัดพระแก้ว)',
            category: 'Attraction',
            cost: 500,
            coords: { top: '30%', left: '35%' },
            note: 'แต่งกายสุภาพ สวมกางเกงขายาว/กระโปรงยาว',
            travelNext: '🚗 เดินทาง 15 นาที (2.5 กม.)'
          },
          {
            id: 'a-2',
            time: '12:00 - 13:30',
            title: 'ทานอาหารกลางวัน ร้านศาลาริมน้ำ',
            category: 'Cafe',
            cost: 450,
            coords: { top: '42%', left: '48%' },
            note: 'แนะจองโต๊ะริมแม่น้ำล่วงหน้า',
            travelNext: '🚶‍♂️ เดินเท้า 5 นาที (300 ม.)'
          },
          {
            id: 'a-3',
            time: '14:00 - 16:00',
            title: 'วัดอรุณราชวราราม ราชวรมหาวิหาร',
            category: 'Attraction',
            cost: 100,
            coords: { top: '58%', left: '62%' },
            note: 'ช่วงบ่ายแสงสวยถ่ายรูปพระปรางค์มุมกว้าง',
            travelNext: '🚗 เดินทาง 20 นาที (6.0 กม.)'
          },
          {
            id: 'a-4',
            time: '17:00 - 20:00',
            title: 'เช็กอิน โรงแรมศาลา อรุณ (Sala Arun)',
            category: 'Stay',
            cost: 3800,
            coords: { top: '75%', left: '78%' },
            note: 'ดินเนอร์ชั้น rooftop ชมพระอาทิตย์ตกดิน',
            travelNext: ''
          }
        ]
      },
      {
        id: 'day2',
        label: 'DAY 2',
        dateStr: '11 พ.ย. 2026',
        title: 'วันที่สอง: คาเฟ่สโลว์ไลฟ์ & ถนนคนเดิน',
        totalDist: '8.2 กม.',
        totalTime: '30 นาที',
        transportMode: '🛵 รถจักรยานยนต์ / เดินเท้า',
        activities: [
          {
            id: 'a-201',
            time: '10:00 - 12:00',
            title: 'คาเฟ่ลายท่า เชียงใหม่ (Lai Tha Cafe)',
            category: 'Cafe',
            cost: 180,
            coords: { top: '28%', left: '32%' },
            note: 'ลองเมนูกาแฟสกัดเย็น Speciality',
            travelNext: '🚗 เดินทาง 10 นาที (3.0 กม.)'
          },
          {
            id: 'a-202',
            time: '16:00 - 19:30',
            title: 'ถนนคนเดินท่าแพ',
            category: 'Souvenir',
            cost: 600,
            coords: { top: '55%', left: '65%' },
            note: 'ซื้อของฝากงานคราฟต์ และทานสตรีทฟู้ด',
            travelNext: ''
          }
        ]
      },
      {
        id: 'day3',
        label: 'DAY 3',
        dateStr: '12 พ.ย. 2026',
        title: 'วันที่สาม: ทะเลใต้ & ชมพระอาทิตย์ตกแหลมพรหมเทพ',
        totalDist: '25.0 กม.',
        totalTime: '50 นาที',
        transportMode: '🚗 รถเช่าขับเอง',
        activities: [
          {
            id: 'a-301',
            time: '16:30 - 18:30',
            title: 'แหลมพรหมเทพ ภูเก็ต',
            category: 'Attraction',
            cost: 0,
            coords: { top: '70%', left: '80%' },
            note: 'ไปถึงก่อน 17:00 น. เพื่อจับจองจุดถ่ายรูป',
            travelNext: ''
          }
        ]
      },
      {
        id: 'day4',
        label: 'DAY 4',
        dateStr: '13 พ.ย. 2026',
        title: 'วันสุดท้าย: ช็อปปิ้งของฝาก & เดินทางกลับ',
        totalDist: '15.0 กม.',
        totalTime: '40 นาที',
        transportMode: '🚗 แท็กซี่สนามบิน',
        activities: [
          {
            id: 'a-401',
            time: '10:00 - 12:00',
            title: 'ซื้อของฝากและขนมท้องถิ่น',
            category: 'Souvenir',
            cost: 1200,
            coords: { top: '40%', left: '50%' },
            note: 'ตรวจสอบน้ำหนักกระเป๋าเดินทาง',
            travelNext: ''
          }
        ]
      }
    ];

    // Helper Function for Badge Styling
    const getCategoryBadgeClass = (category) => {
      switch (category) {
        case 'Attraction':
        case 'สถานที่ท่องเที่ยว':
          return 'bg-blue-50 text-blue-700 border-blue-200';
        case 'Cafe':
        case 'คาเฟ่ & ร้านอาหาร':
          return 'bg-amber-50 text-amber-700 border-amber-200';
        case 'Stay':
        case 'ที่พักแนะนำ':
          return 'bg-purple-50 text-purple-700 border-purple-200';
        case 'Souvenir':
        case 'ของฝาก & ช้อปปิ้ง':
          return 'bg-emerald-50 text-emerald-700 border-emerald-200';
        default:
          return 'bg-slate-50 text-slate-700 border-slate-200';
      }
    };

    // Helper for Generating SVG Path for Map Lines
    const getSvgPath = (activities) => {
      if (!activities || activities.length === 0) return '';
      const points = activities.map(act => {
        const left = parseFloat(act.coords?.left || '50');
        const top = parseFloat(act.coords?.top || '50');
        return `${left} ${top}`;
      });
      return `M ${points.join(' L ')}`;
    };

    // --- MAIN COMBINED APP COMPONENT ---
    function App() {
      // Current View Control: 'search' or 'itinerary'
      const [currentView, setCurrentView] = useState('search');

      // Navigation & Settings
      const [activeMenu, setActiveMenu] = useState('home');
      const [currency, setCurrency] = useState('THB');
      const [language, setLanguage] = useState('TH');

      // Interactive Map States
      const [zoomLevel, setZoomLevel] = useState(2);
      const [selectedProvinceFilter, setSelectedProvinceFilter] = useState('all');
      const [activeMapPopup, setActiveMapPopup] = useState(LOCAL_PLACES[0]);

      // Trip Cart / Saved Places
      const [tripCart, setTripCart] = useState([LOCAL_PLACES[0]]);
      const [isCartOpen, setIsCartOpen] = useState(false);
      const [toastMessage, setToastMessage] = useState('');

      // Search & Filter Form State
      const [destination, setDestination] = useState('bangkok');
      const [startDate, setStartDate] = useState('2026-11-10');
      const [endDate, setEndDate] = useState('2026-11-13');
      const [totalBudget, setTotalBudget] = useState(25000);
      const [adults, setAdults] = useState(2);
      const [childrenCount, setChildrenCount] = useState(0);
      const [selectedStyles, setSelectedStyles] = useState(['ผ่อนคลาย', 'ถ่ายรูป']);

      // Auto Plan Wizard States
      const [isWizardOpen, setIsWizardOpen] = useState(false);
      const [wizardStep, setWizardStep] = useState(1);
      const [wizardStyles, setWizardStyles] = useState(['ผ่อนคลาย', 'ถ่ายรูป']);
      const [wizardTransport, setWizardTransport] = useState('รถยนต์ส่วนตัว / เช่ารถ (เน้นความสะดวก)');
      const [wizardAccOption, setWizardAccOption] = useState('option3');
      const [wizardAccName, setWizardAccName] = useState('');
      const [wizardCustomHotelBudget, setWizardCustomHotelBudget] = useState(2500);
      const [isAnalyzing, setIsAnalyzing] = useState(false);

      // Below Fold Tab & Tool Modals
      const [belowFoldTab, setBelowFoldTab] = useState('Attraction');
      const [activeToolModal, setActiveToolModal] = useState(null);

      // ITINERARY SCHEDULE STATES
      const [daysData, setDaysData] = useState(INITIAL_DAYS_DATA);
      const [activeDayIdx, setActiveDayIdx] = useState(0);
      const [travelerCount, setTravelerCount] = useState(2);
      const [isShareModalOpen, setIsShareModalOpen] = useState(false);
      const [editingActivity, setEditingActivity] = useState(null);
      const [isAddModalOpen, setIsAddModalOpen] = useState(false);
      const [newActivityTitle, setNewActivityTitle] = useState('');
      const [newActivityTime, setNewActivityTime] = useState('14:00 - 15:30');
      const [newActivityCategory, setNewActivityCategory] = useState('Attraction');
      const [newActivityCost, setNewActivityCost] = useState(200);

      const triggerToast = (msg) => {
        setToastMessage(msg);
        setTimeout(() => {
          setToastMessage('');
        }, 3200);
      };

      const addToTripCart = (place) => {
        if (!tripCart.some((p) => p.id === place.id)) {
          setTripCart([...tripCart, place]);
          triggerToast(`เพิ่ม "${place.name}" ลงในทริปของคุณแล้ว! ✨`);
        } else {
          triggerToast(`"${place.name}" อยู่ในแผนท่องเที่ยวของคุณแล้ว`);
        }
      };

      const removeFromTripCart = (placeId) => {
        setTripCart(tripCart.filter((p) => p.id !== placeId));
        triggerToast('ลบสถานที่ออกจากแผนแล้ว');
      };

      const toggleStyleTag = (style) => {
        if (selectedStyles.includes(style)) {
          setSelectedStyles(selectedStyles.filter((s) => s !== style));
        } else {
          setSelectedStyles([...selectedStyles, style]);
        }
      };

      const toggleWizardStyle = (style) => {
        if (wizardStyles.includes(style)) {
          setWizardStyles(wizardStyles.filter((s) => s !== style));
        } else {
          setWizardStyles([...wizardStyles, style]);
        }
      };

      const handleStartDIYPlan = () => {
        setCurrentView('itinerary');
        triggerToast('เริ่มวางแผนท่องเที่ยว DIY! เข้าสู่ตารางแผนเดินทางแล้ว');
      };

      const handleRunAutoWizardAnalysis = () => {
        setIsAnalyzing(true);
        setTimeout(() => {
          setIsAnalyzing(false);
          setIsWizardOpen(false);
          setCurrentView('itinerary');
          triggerToast('จัดแผนท่องเที่ยวสมาร์ตทริปสำเร็จ! ตรวจสอบตารางกิจกรรมของคุณได้เลย 🚀');
        }, 1800);
      };

      // Active Day for Itinerary
      const activeDay = daysData[activeDayIdx] || daysData[0];

      // Calculation for Itinerary Budget
      const totalSpent = daysData.reduce((acc, day) => {
        return acc + day.activities.reduce((aCost, act) => aCost + (act.cost || 0), 0);
      }, 0);

      const overallBudget = totalBudget || 25000;
      const spentPercentage = Math.min(100, Math.round((totalSpent / overallBudget) * 100));
      const avgCostPerPerson = Math.round(totalSpent / Math.max(1, travelerCount));

      // Activity Operations for Itinerary
      const handleMoveActivity = (idx, direction) => {
        const updatedActivities = [...activeDay.activities];
        const targetIdx = direction === 'up' ? idx - 1 : idx + 1;
        if (targetIdx < 0 || targetIdx >= updatedActivities.length) return;
        const temp = updatedActivities[idx];
        updatedActivities[idx] = updatedActivities[targetIdx];
        updatedActivities[targetIdx] = temp;

        const updatedDays = [...daysData];
        updatedDays[activeDayIdx] = { ...activeDay, activities: updatedActivities };
        setDaysData(updatedDays);
        triggerToast('สลับลำดับกิจกรรมแล้ว');
      };

      const handleDeleteActivity = (actId) => {
        const updatedActivities = activeDay.activities.filter(a => a.id !== actId);
        const updatedDays = [...daysData];
        updatedDays[activeDayIdx] = { ...activeDay, activities: updatedActivities };
        setDaysData(updatedDays);
        triggerToast('ลบกิจกรรมออกจากตารางเรียบร้อยแล้ว');
      };

      const handleSaveEditActivity = () => {
        if (!editingActivity) return;
        const updatedActivities = activeDay.activities.map(a => a.id === editingActivity.id ? editingActivity : a);
        const updatedDays = [...daysData];
        updatedDays[activeDayIdx] = { ...activeDay, activities: updatedActivities };
        setDaysData(updatedDays);
        setEditingActivity(null);
        triggerToast('อัปเดตรายละเอียดกิจกรรมเรียบร้อยแล้ว');
      };

      const handleAddActivity = () => {
        if (!newActivityTitle.trim()) {
          triggerToast('กรุณาระบุชื่อกิจกรรม');
          return;
        }
        const newAct = {
          id: `act-${Date.now()}`,
          time: newActivityTime,
          title: newActivityTitle,
          category: newActivityCategory,
          cost: Number(newActivityCost) || 0,
          coords: { top: `${Math.floor(Math.random() * 60) + 20}%`, left: `${Math.floor(Math.random() * 60) + 20}%` },
          note: 'เพิ่มใหม่โดยผู้ใช้',
          travelNext: '🚗 เดินทาง 15 นาที'
        };
        const updatedDays = [...daysData];
        updatedDays[activeDayIdx] = {
          ...activeDay,
          activities: [...activeDay.activities, newAct]
        };
        setDaysData(updatedDays);
        setIsAddModalOpen(false);
        setNewActivityTitle('');
        triggerToast(`เพิ่ม "${newAct.title}" เข้าใน ${activeDay.label} แล้ว`);
      };

      const handleOptimizeRoute = () => {
        triggerToast('⚡ ประมวลผลจัดเส้นทางเดินทางที่ดีที่สุดสำหรับวันนี้แล้ว!');
      };

      const filteredLocalPlaces = LOCAL_PLACES.filter((p) => {
        if (selectedProvinceFilter === 'all') return true;
        return p.provinceId === selectedProvinceFilter;
      });

      return (
        <div className="min-h-screen bg-[#F8FAFC] text-slate-800 flex flex-col font-sans antialiased">
          
          {/* TOAST NOTIFICATION BANNER */}
          {toastMessage && (
            <div className="fixed top-5 right-5 z-50 bg-[#0B192C] text-white px-5 py-3.5 rounded-2xl shadow-2xl flex items-center gap-3 border border-blue-500/30 animate-bounce">
              <span className="text-xl">✨</span>
              <span className="font-medium text-sm">{toastMessage}</span>
            </div>
          )}

          {/* TOP GLOBAL HEADER BAR */}
          <header className="h-16 bg-[#0B192C] border-b border-slate-800 text-white px-4 lg:px-8 flex items-center justify-between sticky top-0 z-40 shadow-md">
            <div className="flex items-center gap-4">
              <div 
                onClick={() => setCurrentView('search')}
                className="flex items-center gap-2.5 cursor-pointer group"
              >
                <div className="w-10 h-10 rounded-xl bg-gradient-to-tr from-blue-600 to-indigo-500 flex items-center justify-center font-black text-xl text-white shadow-lg shadow-blue-500/20 group-hover:scale-105 transition-transform">
                  U
                </div>
                <div>
                  <div className="font-bold tracking-tight text-lg leading-tight flex items-center gap-1.5">
                    <span>UPlan</span>
                    <span className="text-xs px-2 py-0.5 rounded-full bg-blue-500/20 text-blue-400 font-medium border border-blue-400/30">
                      PRO
                    </span>
                  </div>
                  <div className="text-[11px] text-slate-400 font-light">Smart Travel Planner Platform</div>
                </div>
              </div>

              {/* View Nav Tabs */}
              <div className="hidden md:flex items-center bg-slate-800/90 rounded-xl p-1 border border-slate-700/60 ml-4">
                <button
                  onClick={() => setCurrentView('search')}
                  className={`px-3.5 py-1.5 rounded-lg text-xs font-semibold transition-all flex items-center gap-1.5 ${
                    currentView === 'search'
                      ? 'bg-blue-600 text-white shadow-md'
                      : 'text-slate-300 hover:text-white hover:bg-slate-700/50'
                  }`}
                >
                  <span>🗺️ ค้นหา & จัดทริป</span>
                </button>
                <button
                  onClick={() => setCurrentView('itinerary')}
                  className={`px-3.5 py-1.5 rounded-lg text-xs font-semibold transition-all flex items-center gap-1.5 ${
                    currentView === 'itinerary'
                      ? 'bg-blue-600 text-white shadow-md'
                      : 'text-slate-300 hover:text-white hover:bg-slate-700/50'
                  }`}
                >
                  <span>📅 ตารางเดินทาง</span>
                  <span className="bg-emerald-500 text-white px-1.5 py-0.2 rounded-full text-[10px]">
                    {daysData.reduce((acc, d) => acc + d.activities.length, 0)}
                  </span>
                </button>
              </div>
            </div>

            {/* Header Right Utilities */}
            <div className="flex items-center gap-3">
              {/* Trip Cart Trigger */}
              <button
                onClick={() => setIsCartOpen(!isCartOpen)}
                className="relative px-3.5 py-2 rounded-xl bg-blue-600/90 hover:bg-blue-600 text-white text-xs font-semibold flex items-center gap-2 transition-all shadow-md hover:shadow-blue-500/20 active:scale-95"
              >
                <span>🎒 ทริปของฉัน</span>
                <span className="bg-white text-blue-700 rounded-full px-2 py-0.5 font-bold text-[11px] shadow-inner">
                  {tripCart.length}
                </span>
              </button>

              {/* Quick Auto Plan Wizard Launch */}
              <button
                onClick={() => {
                  setWizardStep(1);
                  setIsWizardOpen(true);
                }}
                className="hidden sm:flex px-3.5 py-2 rounded-xl bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-600 hover:to-teal-700 text-white text-xs font-semibold items-center gap-1.5 transition-all shadow-md shadow-emerald-500/20 active:scale-95"
              >
                <span>⚡ Auto Plan Wizard</span>
              </button>

              {/* Language & Currency Switches */}
              <div className="hidden md:flex items-center bg-slate-800/80 rounded-xl p-1 border border-slate-700/60 text-xs">
                <button
                  onClick={() => setCurrency(currency === 'THB' ? 'USD' : 'THB')}
                  className="px-2.5 py-1 rounded-lg font-medium text-slate-300 hover:text-white transition-colors"
                >
                  {currency === 'THB' ? '฿ THB' : '$ USD'}
                </button>
                <div className="w-[1px] h-4 bg-slate-700 mx-0.5"></div>
                <button
                  onClick={() => setLanguage(language === 'TH' ? 'EN' : 'TH')}
                  className="px-2.5 py-1 rounded-lg font-medium text-slate-300 hover:text-white transition-colors"
                >
                  {language === 'TH' ? '🇹🇭 TH' : '🇺🇸 EN'}
                </button>
              </div>

              {/* User Profile Avatar */}
              <div className="w-9 h-9 rounded-xl bg-slate-700 border border-slate-600 overflow-hidden cursor-pointer flex items-center justify-center text-xs font-bold text-white hover:ring-2 hover:ring-blue-500 transition-all">
                <img
                  src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=120&q=80"
                  alt="User profile"
                  className="w-full h-full object-cover"
                />
              </div>
            </div>
          </header>

          {/* MAIN APPLICATION BODY */}
          <div className="flex-1 flex overflow-hidden">

            {/* LEFT SIDEBAR NAVIGATION */}
            <aside className="w-64 bg-[#0B192C] text-slate-300 border-r border-slate-800 flex-col justify-between hidden lg:flex shrink-0">
              <div className="p-4 space-y-6 overflow-y-auto">
                
                {/* GROUP 1: BOOKING & TRAVEL SERVICES */}
                <div>
                  <div className="text-[11px] font-bold text-slate-400 uppercase tracking-wider mb-2.5 px-2">
                    1. Booking & Travel Services
                  </div>
                  <nav className="space-y-1">
                    {[
                      { id: 'hotels', label: 'โรงแรม & ที่พัก', icon: '🏨', desc: 'ค้นหาและจองที่พัก' },
                      { id: 'flights', label: 'ตั๋วเครื่องบิน', icon: '✈️', desc: 'เปรียบเทียบราคาตั๋ว' },
                      { id: 'cars', label: 'รถเช่า & การเดินทาง', icon: '🚗', desc: 'รถเช่าและรถรับส่ง' },
                      { id: 'attractions', label: 'บัตรท่องเที่ยว & ทัวร์', icon: '🎟️', desc: 'ซื้อบัตรเข้าชม' },
                      { id: 'sim', label: 'ซิมการ์ด & Pocket WiFi', icon: '📶', desc: 'อินเทอร์เน็ตเดินทาง' },
                      { id: 'insurance', label: 'ประกันการเดินทาง', icon: '🛡️', desc: 'ความคุ้มครองตลอดทริป' },
                    ].map((item) => (
                      <button
                        key={item.id}
                        onClick={() => {
                          setActiveMenu(item.id);
                          setActiveToolModal(item);
                        }}
                        className={`w-full flex items-center gap-3 px-3 py-2.5 rounded-xl text-xs font-medium transition-all text-left group ${
                          activeMenu === item.id
                            ? 'bg-[#0066FF] text-white shadow-md shadow-blue-600/30 font-semibold'
                            : 'hover:bg-slate-800/80 text-slate-300'
                        }`}
                      >
                        <span className="text-base group-hover:scale-110 transition-transform">{item.icon}</span>
                        <span className="flex-1 truncate">{item.label}</span>
                      </button>
                    ))}
                  </nav>
                </div>

                {/* GROUP 2: TRAVEL HELPER TOOLS */}
                <div>
                  <div className="text-[11px] font-bold text-slate-400 uppercase tracking-wider mb-2.5 px-2">
                    2. Travel Helper Tools
                  </div>
                  <nav className="space-y-1">
                    {[
                      { id: 'budget', label: 'คำนวณงบ & หารค่าใช้จ่าย', icon: '🧮', desc: 'Budget & Split Bill' },
                      { id: 'checklist', label: 'รายการเตรียมตัวส่วนตัว', icon: '🧳', desc: 'Personal Checklist' },
                      { id: 'guides', label: 'ไกด์ท้องถิ่นนำเที่ยว', icon: '👨‍💼', desc: 'Local Tour Guides' },
                    ].map((item) => (
                      <button
                        key={item.id}
                        onClick={() => {
                          setActiveMenu(item.id);
                          setActiveToolModal(item);
                        }}
                        className={`w-full flex items-center gap-3 px-3 py-2.5 rounded-xl text-xs font-medium transition-all text-left group ${
                          activeMenu === item.id
                            ? 'bg-[#0066FF] text-white shadow-md shadow-blue-600/30 font-semibold'
                            : 'hover:bg-slate-800/80 text-slate-300'
                        }`}
                      >
                        <span className="text-base group-hover:scale-110 transition-transform">{item.icon}</span>
                        <span className="flex-1 truncate">{item.label}</span>
                      </button>
                    ))}
                  </nav>
                </div>

                {/* GROUP 3: ACCOUNT & SETTINGS */}
                <div>
                  <div className="text-[11px] font-bold text-slate-400 uppercase tracking-wider mb-2.5 px-2">
                    3. Account & Settings
                  </div>
                  <nav className="space-y-1">
                    {[
                      { id: 'profile', label: 'โปรไฟล์ของฉัน', icon: '👤' },
                      { id: 'settings', label: 'ภาษา & สกุลเงิน', icon: '💱' },
                      { id: 'notifications', label: 'การแจ้งเตือน', icon: '🔔' },
                      { id: 'help', label: 'ศูนย์ช่วยเหลือ & ติดต่อ', icon: '❓' },
                    ].map((item) => (
                      <button
                        key={item.id}
                        onClick={() => {
                          setActiveMenu(item.id);
                          setActiveToolModal(item);
                        }}
                        className={`w-full flex items-center gap-3 px-3 py-2.5 rounded-xl text-xs font-medium transition-all text-left ${
                          activeMenu === item.id
                            ? 'bg-[#0066FF] text-white shadow-md font-semibold'
                            : 'hover:bg-slate-800/80 text-slate-300'
                        }`}
                      >
                        <span className="text-base">{item.icon}</span>
                        <span className="flex-1 truncate">{item.label}</span>
                      </button>
                    ))}
                  </nav>
                </div>

              </div>

              {/* Sidebar Footer User Card */}
              <div className="p-4 border-t border-slate-800 bg-slate-900/60">
                <div className="flex items-center gap-3">
                  <div className="w-8 h-8 rounded-full bg-blue-600/30 text-blue-400 border border-blue-500/30 flex items-center justify-center font-bold text-xs">
                    U
                  </div>
                  <div className="flex-1 min-w-0">
                    <div className="text-xs font-semibold text-white truncate">ผู้ใช้งาน UPlan Member</div>
                    <div className="text-[10px] text-slate-400 truncate">member@uplan.travel</div>
                  </div>
                </div>
              </div>
            </aside>

            {/* MAIN CONTENT AREA */}
            <main className="flex-1 overflow-y-auto bg-[#F8FAFC]">
              
              {/* VIEW 1: SEARCH & INTERACTIVE MAP VIEW */}
              {currentView === 'search' && (
                <div className="animate-in fade-in duration-200">
                  <section className="p-4 lg:p-6 max-w-[1600px] mx-auto">
                    
                    <div className="mb-4 flex flex-col md:flex-row md:items-center justify-between gap-3">
                      <div>
                        <h1 className="text-xl lg:text-2xl font-bold text-slate-900 tracking-tight flex items-center gap-2">
                          <span>วางแผนท่องเที่ยวไทยด้วย AI สมาร์ตทริป</span>
                          <span className="text-xs font-normal px-2.5 py-1 rounded-full bg-blue-100 text-blue-700 border border-blue-200">
                            Interactive Map
                          </span>
                        </h1>
                        <p className="text-xs text-slate-500 mt-1">
                          เลือกหมุดสถานที่บนแผนที่ ค้นหาแพ็กเกจ หรือใช้ Auto Plan Wizard สร้างแผนเที่ยวอัตโนมัติ
                        </p>
                      </div>

                      {/* Mobile View Navigation Toggle */}
                      <div className="lg:hidden flex items-center bg-slate-200 p-1 rounded-xl text-xs font-medium">
                        <button 
                          onClick={() => setCurrentView('search')}
                          className={`flex-1 py-1.5 px-3 rounded-lg font-semibold ${currentView === 'search' ? 'bg-white text-blue-600 shadow-sm' : 'text-slate-600'}`}
                        >
                          แผนที่ & ค้นหา
                        </button>
                        <button
                          onClick={() => setCurrentView('itinerary')}
                          className={`flex-1 py-1.5 px-3 rounded-lg font-semibold ${currentView === 'itinerary' ? 'bg-white text-blue-600 shadow-sm' : 'text-slate-600'}`}
                        >
                          ตารางเดินทาง
                        </button>
                      </div>
                    </div>

                    {/* SPLIT SCREEN GRID: LEFT MAP (7 COLS) | RIGHT SEARCH PANE (5 COLS) */}
                    <div className="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
                      
                      {/* LEFT INTERACTIVE CLUSTERED MAP CONTAINER */}
                      <div className="lg:col-span-7 bg-white rounded-2xl border border-slate-200 shadow-xl shadow-slate-200/50 overflow-hidden flex flex-col h-[620px] relative">
                        
                        {/* MAP CONTROLS HEADER */}
                        <div className="p-3 bg-slate-900 text-white flex flex-wrap items-center justify-between gap-2 z-10">
                          <div className="flex items-center gap-1.5 text-xs">
                            <span className="text-slate-400 font-medium hidden sm:inline">ระดับการย่อ/ขยาย:</span>
                            <div className="flex bg-slate-800 rounded-lg p-0.5 border border-slate-700">
                              <button
                                onClick={() => setZoomLevel(1)}
                                className={`px-2.5 py-1 rounded-md text-[11px] font-medium transition-colors ${
                                  zoomLevel === 1 ? 'bg-blue-600 text-white font-bold' : 'text-slate-300 hover:text-white'
                                }`}
                              >
                                ระดับ 1: รายจังหวัด
                              </button>
                              <button
                                onClick={() => setZoomLevel(2)}
                                className={`px-2.5 py-1 rounded-md text-[11px] font-medium transition-colors ${
                                  zoomLevel === 2 ? 'bg-blue-600 text-white font-bold' : 'text-slate-300 hover:text-white'
                                }`}
                              >
                                ระดับ 2: ภูมิภาค
                              </button>
                              <button
                                onClick={() => setZoomLevel(3)}
                                className={`px-2.5 py-1 rounded-md text-[11px] font-medium transition-colors ${
                                  zoomLevel === 3 ? 'bg-blue-600 text-white font-bold' : 'text-slate-300 hover:text-white'
                                }`}
                              >
                                ระดับ 3: หมุดเจาะจง
                              </button>
                            </div>
                          </div>

                          {/* Province Quick Filter */}
                          <div className="flex items-center gap-2">
                            <select
                              value={selectedProvinceFilter}
                              onChange={(e) => setSelectedProvinceFilter(e.target.value)}
                              className="bg-slate-800 text-slate-200 text-xs px-2.5 py-1 rounded-lg border border-slate-700 focus:outline-none focus:ring-1 focus:ring-blue-500"
                            >
                              {PROVINCES_DATA.map((prov) => (
                                <option key={prov.id} value={prov.id}>
                                  {prov.icon} {prov.name}
                                </option>
                              ))}
                            </select>

                            <button
                              onClick={() => {
                                setZoomLevel(2);
                                setSelectedProvinceFilter('all');
                              }}
                              className="text-xs bg-slate-800 hover:bg-slate-700 text-slate-300 px-2 py-1 rounded-lg border border-slate-700 transition-colors"
                              title="รีเซ็ตแผนที่"
                            >
                              🔄 รีเซ็ต
                            </button>
                          </div>
                        </div>

                        {/* CANVAS STYLED MAP AREA */}
                        <div className="flex-1 bg-[#E0EDF8] relative overflow-hidden select-none cursor-grab active:cursor-grabbing">
                          
                          {/* Map Grid Pattern Background */}
                          <div className="absolute inset-0 opacity-20 pointer-events-none bg-[radial-gradient(#0066FF_1px,transparent_1px)] [background-size:16px_16px]"></div>
                          
                          {/* Decorative Coastline */}
                          <svg className="absolute inset-0 w-full h-full opacity-30 pointer-events-none stroke-blue-400 fill-blue-100" viewBox="0 0 500 600">
                            <path d="M 150,50 Q 200,120 230,200 T 250,350 T 210,500 T 180,580" fill="none" strokeWidth="2" strokeDasharray="4 4" />
                            <circle cx="230" cy="270" r="140" fill="#CBD5E1" opacity="0.3" />
                          </svg>

                          {/* Map Legend Overlay Badge */}
                          <div className="absolute bottom-3 left-3 bg-white/90 backdrop-blur-md px-3 py-1.5 rounded-xl text-[11px] font-medium text-slate-700 border border-slate-200 shadow-sm z-10 flex items-center gap-2">
                            <span className="w-2 h-2 rounded-full bg-blue-600 animate-pulse"></span>
                            <span>
                              {zoomLevel === 1 && 'แสดงมุมมองภาพรวมทั้งประเทศ (Macro Pins)'}
                              {zoomLevel === 2 && 'แสดงการกระจายหมุดสถานที่แนะนำ (Regional View)'}
                              {zoomLevel === 3 && 'แสดงหมุดสถานที่ละเอียดพร้อมราคา (Micro Detail Pins)'}
                            </span>
                          </div>

                          {/* ZOOM LEVEL 1: MACRO PROVINCE PINS */}
                          {zoomLevel === 1 && (
                            <div className="absolute inset-0">
                              {MACRO_PINS.filter(
                                (m) => selectedProvinceFilter === 'all' || m.provinceId === selectedProvinceFilter
                              ).map((macro) => (
                                <div
                                  key={macro.id}
                                  style={macro.coords}
                                  onClick={() => {
                                    setSelectedProvinceFilter(macro.provinceId);
                                    setZoomLevel(2);
                                    triggerToast(`เข้าสู่มุมมองจังหวัด ${macro.name}`);
                                  }}
                                  className="absolute -translate-x-1/2 -translate-y-1/2 cursor-pointer group z-20"
                                >
                                  <div className="bg-white hover:bg-slate-900 hover:text-white rounded-2xl p-2.5 shadow-xl border border-slate-200/80 transition-all transform hover:scale-110 flex items-center gap-3">
                                    <div className="w-10 h-10 rounded-xl overflow-hidden relative shrink-0">
                                      <img src={macro.image} alt={macro.name} className="w-full h-full object-cover" />
                                    </div>
                                    <div>
                                      <div className="font-bold text-xs flex items-center gap-1">
                                        <span>{macro.icon}</span>
                                        <span>{macro.name}</span>
                                      </div>
                                      <div className="text-[10px] text-blue-600 group-hover:text-blue-300 font-medium">
                                        {macro.placesCount}+ สถานที่น่าเที่ยว
                                      </div>
                                    </div>
                                    <span className="text-slate-400 group-hover:text-white text-xs">➔</span>
                                  </div>
                                </div>
                              ))}
                            </div>
                          )}

                          {/* ZOOM LEVEL 2 & 3: LOCAL PLACES PREVIEW PINS */}
                          {(zoomLevel === 2 || zoomLevel === 3) && (
                            <div className="absolute inset-0">
                              {filteredLocalPlaces.map((place) => (
                                <div
                                  key={place.id}
                                  style={place.coords}
                                  onClick={() => setActiveMapPopup(place)}
                                  className={`absolute -translate-x-1/2 -translate-y-1/2 cursor-pointer transition-all z-20 group ${
                                    activeMapPopup?.id === place.id ? 'z-30 scale-105' : 'hover:scale-110'
                                  }`}
                                >
                                  {zoomLevel === 2 ? (
                                    <div className="bg-slate-900 text-white rounded-full px-3 py-1 text-[11px] font-semibold shadow-lg border border-blue-400 flex items-center gap-1.5 hover:bg-blue-600 transition-colors">
                                      <span className="w-2 h-2 rounded-full bg-emerald-400"></span>
                                      <span className="truncate max-w-[100px]">{place.name}</span>
                                      <span className="text-blue-300 bg-slate-800 px-1.5 py-0.2 rounded-md text-[10px]">
                                        {place.price}
                                      </span>
                                    </div>
                                  ) : (
                                    <div className="bg-white rounded-xl p-1.5 shadow-xl border-2 border-blue-500 flex items-center gap-2 max-w-[160px]">
                                      <img src={place.image} alt={place.name} className="w-8 h-8 rounded-lg object-cover" />
                                      <div className="min-w-0 flex-1">
                                        <div className="text-[10px] font-bold text-slate-800 truncate">{place.name}</div>
                                        <div className="text-[9px] text-blue-600 font-semibold">{place.price}</div>
                                      </div>
                                    </div>
                                  )}
                                </div>
                              ))}
                            </div>
                          )}

                          {/* INTERACTIVE POP-UP CARD OVERLAY */}
                          {activeMapPopup && (
                            <div className="absolute bottom-6 right-6 left-6 sm:left-auto sm:w-[320px] bg-white rounded-2xl shadow-2xl border border-slate-200/90 overflow-hidden z-40 animate-in fade-in slide-in-from-bottom-4 duration-200">
                              <div className="h-36 relative overflow-hidden group">
                                <img
                                  src={activeMapPopup.image}
                                  alt={activeMapPopup.name}
                                  className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
                                />
                                <div className="absolute inset-0 bg-gradient-to-t from-slate-900/80 via-transparent to-black/30"></div>
                                
                                <button
                                  onClick={() => setActiveMapPopup(null)}
                                  className="absolute top-2.5 right-2.5 w-7 h-7 rounded-full bg-black/50 hover:bg-black text-white text-xs flex items-center justify-center transition-colors"
                                >
                                  ✕
                                </button>

                                <div className="absolute top-2.5 left-2.5 flex items-center gap-1.5">
                                  <span className="bg-blue-600 text-white text-[10px] font-bold px-2 py-0.5 rounded-full shadow-sm">
                                    {activeMapPopup.categoryName}
                                  </span>
                                  <span className="bg-emerald-500/90 text-white text-[10px] font-semibold px-2 py-0.5 rounded-full backdrop-blur-sm">
                                    {activeMapPopup.tag}
                                  </span>
                                </div>

                                <div className="absolute bottom-2.5 left-2.5 text-white text-xs font-bold flex items-center gap-1">
                                  <span className="text-amber-400">⭐ {activeMapPopup.rating}</span>
                                  <span className="text-slate-300 font-normal text-[10px]">
                                    ({activeMapPopup.reviews.toLocaleString()} รีวิว)
                                  </span>
                                </div>
                              </div>

                              <div className="p-3.5">
                                <h3 className="font-bold text-sm text-slate-900 leading-snug line-clamp-1">
                                  {activeMapPopup.name}
                                </h3>
                                <p className="text-[11px] text-slate-500 mt-1 line-clamp-2 leading-relaxed">
                                  {activeMapPopup.subtext}
                                </p>

                                <div className="mt-3.5 pt-2.5 border-t border-slate-100 flex items-center justify-between">
                                  <div>
                                    <span className="text-[10px] text-slate-400 block">ราคาเริ่มต้น / ค่าเข้า</span>
                                    <span className="text-base font-extrabold text-blue-600">
                                      {activeMapPopup.price}
                                    </span>
                                  </div>

                                  <button
                                    onClick={() => addToTripCart(activeMapPopup)}
                                    className="px-4 py-2 rounded-xl bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white text-xs font-bold shadow-md shadow-blue-500/25 transition-all hover:scale-105 active:scale-95 flex items-center gap-1.5"
                                  >
                                    <span>+ ใส่ทริปนี้</span>
                                  </button>
                                </div>
                              </div>
                            </div>
                          )}

                        </div>
                      </div>

                      {/* RIGHT SEARCH & FILTER PANE CONTAINER */}
                      <div className="lg:col-span-5 bg-white rounded-2xl border border-slate-200 p-5 shadow-xl shadow-slate-200/50 space-y-5">
                        
                        <div className="flex items-center justify-between border-b border-slate-100 pb-3">
                          <div>
                            <h2 className="font-bold text-lg text-slate-900 flex items-center gap-2">
                              <span>🎯 ค้นหา & ออกแบบทริป</span>
                            </h2>
                            <p className="text-xs text-slate-500">ระบุรายละเอียดการเดินทางเพื่อเริ่มต้นจัดแพลน</p>
                          </div>
                          <span className="px-2.5 py-1 rounded-full bg-emerald-50 text-emerald-700 text-[11px] font-semibold border border-emerald-200">
                            AI Guided
                          </span>
                        </div>

                        {/* SEARCH FORM FIELDS */}
                        <div className="space-y-4">
                          
                          {/* Destination Dropdown */}
                          <div>
                            <label className="block text-xs font-bold text-slate-700 mb-1.5">
                              📍 จุดหมายปลายทาง (Destination)
                            </label>
                            <select
                              value={destination}
                              onChange={(e) => {
                                setDestination(e.target.value);
                                setSelectedProvinceFilter(e.target.value);
                              }}
                              className="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-2.5 text-xs font-medium text-slate-800 focus:ring-2 focus:ring-blue-500 focus:outline-none transition-all"
                            >
                              {PROVINCES_DATA.map((prov) => (
                                <option key={prov.id} value={prov.id}>
                                  {prov.icon} {prov.name}
                                </option>
                              ))}
                            </select>
                          </div>

                          {/* Travel Dates Picker */}
                          <div className="grid grid-cols-2 gap-3">
                            <div>
                              <label className="block text-xs font-bold text-slate-700 mb-1.5">
                                📅 วันเดินทางไป
                              </label>
                              <input
                                type="date"
                                value={startDate}
                                onChange={(e) => setStartDate(e.target.value)}
                                className="w-full bg-slate-50 border border-slate-300 rounded-xl px-3 py-2 text-xs font-medium text-slate-800 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                              />
                            </div>
                            <div>
                              <label className="block text-xs font-bold text-slate-700 mb-1.5">
                                🏁 วันเดินทางกลับ
                              </label>
                              <input
                                type="date"
                                value={endDate}
                                onChange={(e) => setEndDate(e.target.value)}
                                className="w-full bg-slate-50 border border-slate-300 rounded-xl px-3 py-2 text-xs font-medium text-slate-800 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                              />
                            </div>
                          </div>

                          {/* Total Budget Slider */}
                          <div>
                            <div className="flex items-center justify-between mb-1.5">
                              <label className="text-xs font-bold text-slate-700">
                                💰 งบประมาณรวมทั้งทริป (Total Budget)
                              </label>
                              <span className="text-sm font-extrabold text-blue-600 bg-blue-50 px-2.5 py-0.5 rounded-lg border border-blue-200">
                                {totalBudget.toLocaleString()} THB
                              </span>
                            </div>
                            <input
                              type="range"
                              min="5000"
                              max="100000"
                              step="1000"
                              value={totalBudget}
                              onChange={(e) => setTotalBudget(Number(e.target.value))}
                              className="w-full h-2 bg-slate-200 rounded-lg appearance-none cursor-pointer accent-blue-600"
                            />
                            <div className="flex justify-between text-[10px] text-slate-400 mt-1">
                              <span>5,000 THB</span>
                              <span>50,000 THB</span>
                              <span>100,000 THB</span>
                            </div>
                          </div>

                          {/* Headcount Selector */}
                          <div>
                            <label className="block text-xs font-bold text-slate-700 mb-1.5">
                              👥 จำนวนผู้เดินทาง (Headcount)
                            </label>
                            <div className="grid grid-cols-2 gap-3 bg-slate-50 p-2.5 rounded-xl border border-slate-200">
                              
                              {/* Adults Counter */}
                              <div className="flex items-center justify-between">
                                <div>
                                  <div className="text-xs font-semibold text-slate-800">ผู้ใหญ่</div>
                                  <div className="text-[10px] text-slate-400">อายุ 12 ปีขึ้นไป</div>
                                </div>
                                <div className="flex items-center gap-2">
                                  <button
                                    onClick={() => setAdults(Math.max(1, adults - 1))}
                                    className="w-6 h-6 rounded-lg bg-white border border-slate-300 text-slate-700 font-bold text-xs flex items-center justify-center hover:bg-slate-100"
                                  >
                                    -
                                  </button>
                                  <span className="text-xs font-bold w-4 text-center">{adults}</span>
                                  <button
                                    onClick={() => setAdults(adults + 1)}
                                    className="w-6 h-6 rounded-lg bg-white border border-slate-300 text-slate-700 font-bold text-xs flex items-center justify-center hover:bg-slate-100"
                                  >
                                    +
                                  </button>
                                </div>
                              </div>

                              {/* Children Counter */}
                              <div className="flex items-center justify-between">
                                <div>
                                  <div className="text-xs font-semibold text-slate-800">เด็ก</div>
                                  <div className="text-[10px] text-slate-400">อายุต่ำกว่า 12 ปี</div>
                                </div>
                                <div className="flex items-center gap-2">
                                  <button
                                    onClick={() => setChildrenCount(Math.max(0, childrenCount - 1))}
                                    className="w-6 h-6 rounded-lg bg-white border border-slate-300 text-slate-700 font-bold text-xs flex items-center justify-center hover:bg-slate-100"
                                  >
                                    -
                                  </button>
                                  <span className="text-xs font-bold w-4 text-center">{childrenCount}</span>
                                  <button
                                    onClick={() => setChildrenCount(childrenCount + 1)}
                                    className="w-6 h-6 rounded-lg bg-white border border-slate-300 text-slate-700 font-bold text-xs flex items-center justify-center hover:bg-slate-100"
                                  >
                                    +
                                  </button>
                                </div>
                              </div>

                            </div>
                          </div>

                          {/* Travel Style Multi-Select Chips */}
                          <div>
                            <label className="block text-xs font-bold text-slate-700 mb-1.5">
                              ✨ สไตล์การเที่ยวที่ชอบ
                            </label>
                            <div className="flex flex-wrap gap-1.5">
                              {[
                                '☀️ ผ่อนคลาย',
                                '📸 ถ่ายรูป',
                                '🍜 สายกิน',
                                '🌲 สายลุย',
                                '🏛️ วัฒนธรรม',
                                '🛍️ ช้อปปิ้ง'
                              ].map((style) => {
                                const cleanLabel = style.replace(/^[^\s]+\s/, '');
                                const isSelected = selectedStyles.includes(cleanLabel);
                                return (
                                  <button
                                    key={style}
                                    type="button"
                                    onClick={() => toggleStyleTag(cleanLabel)}
                                    className={`px-3 py-1.5 rounded-xl text-xs font-medium transition-all ${
                                      isSelected
                                        ? 'bg-blue-600 text-white shadow-md shadow-blue-500/20 font-semibold'
                                        : 'bg-slate-100 text-slate-600 hover:bg-slate-200'
                                    }`}
                                  >
                                    {style}
                                  </button>
                                );
                              })}
                            </div>
                          </div>

                        </div>

                        {/* 2 MAIN TRIGGER BUTTONS: DIY PLAN & AUTO PLAN WIZARD */}
                        <div className="pt-2 grid grid-cols-2 gap-3">
                          <button
                            onClick={handleStartDIYPlan}
                            className="w-full py-3 px-4 rounded-xl border-2 border-slate-800 hover:bg-slate-900 hover:text-white text-slate-800 font-bold text-xs transition-all shadow-sm flex items-center justify-center gap-1.5 active:scale-95"
                          >
                            <span>🛠️ DIY Plan</span>
                          </button>

                          <button
                            onClick={() => {
                              setWizardStep(1);
                              setIsWizardOpen(true);
                            }}
                            className="w-full py-3 px-4 rounded-xl bg-gradient-to-r from-blue-600 via-indigo-600 to-emerald-600 hover:opacity-95 text-white font-bold text-xs transition-all shadow-lg shadow-blue-500/25 flex items-center justify-center gap-1.5 active:scale-95"
                          >
                            <span>⚡ Auto Plan Wizard</span>
                          </button>
                        </div>

                      </div>

                    </div>

                  </section>

                  {/* BELOW THE FOLD CONTENT SECTION */}
                  <section className="p-4 lg:p-6 max-w-[1600px] mx-auto space-y-8 border-t border-slate-200 mt-6">
                    
                    {/* 1. TRENDING DESTINATIONS GRID */}
                    <div>
                      <div className="flex items-center justify-between mb-4">
                        <div>
                          <h2 className="text-lg font-bold text-slate-900 tracking-tight">
                            🔥 จุดหมายปลายทางยอดฮิต (Trending Destinations)
                          </h2>
                          <p className="text-xs text-slate-500">จังหวัดน่าเที่ยวที่มีผู้ใช้งานสร้างแผนเที่ยวมากที่สุด</p>
                        </div>
                        <button className="text-xs font-semibold text-blue-600 hover:text-blue-800 flex items-center gap-1">
                          <span>ดูทั้งหมด</span>
                          <span>➔</span>
                        </button>
                      </div>

                      <div className="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-5 gap-4">
                        {MACRO_PINS.map((dest) => (
                          <div
                            key={dest.id}
                            onClick={() => {
                              setSelectedProvinceFilter(dest.provinceId);
                              setZoomLevel(2);
                              window.scrollTo({ top: 0, behavior: 'smooth' });
                            }}
                            className="bg-white rounded-2xl border border-slate-200 overflow-hidden shadow-sm hover:shadow-xl transition-all cursor-pointer group"
                          >
                            <div className="h-32 relative overflow-hidden">
                              <img
                                src={dest.image}
                                alt={dest.name}
                                className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300"
                              />
                              <div className="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent"></div>
                              <span className="absolute top-2.5 left-2.5 bg-black/40 backdrop-blur-md text-white text-[10px] px-2 py-0.5 rounded-full">
                                {dest.icon} {dest.enName}
                              </span>
                            </div>
                            <div className="p-3">
                              <h3 className="font-bold text-xs text-slate-900">{dest.name}</h3>
                              <div className="text-[10px] text-blue-600 font-semibold mt-0.5">
                                {dest.placesCount}+ สถานที่น่าเที่ยว
                              </div>
                              <div className="text-[10px] text-slate-400 mt-1">งบเฉลี่ย: {dest.avgBudget}</div>
                            </div>
                          </div>
                        ))}
                      </div>
                    </div>

                    {/* 2. RECOMMENDED PLACES CAROUSEL */}
                    <div>
                      <div className="flex flex-col sm:flex-row sm:items-center justify-between gap-3 mb-4">
                        <div>
                          <h2 className="text-lg font-bold text-slate-900 tracking-tight">
                            ⭐ สถานที่แนะนำประจำสัปดาห์ (Recommended Places)
                          </h2>
                          <p className="text-xs text-slate-500">คัดสรรสถานที่ท่องเที่ยวยอดนิยม ร้านอาหารเด็ด และที่พักคุณภาพ</p>
                        </div>

                        <div className="flex items-center gap-1.5 overflow-x-auto pb-1 sm:pb-0">
                          {[
                            { id: 'Attraction', label: '🏛️ สถานที่ท่องเที่ยว' },
                            { id: 'Stay', label: '🏨 ที่พักแนะนำ' },
                            { id: 'Cafe', label: '☕ คาเฟ่ & ร้านอาหาร' },
                            { id: 'Souvenir', label: '🎁 ของฝาก & ช้อปปิ้ง' },
                          ].map((cat) => (
                            <button
                              key={cat.id}
                              onClick={() => setBelowFoldTab(cat.id)}
                              className={`px-3 py-1.5 rounded-xl text-xs font-semibold shrink-0 transition-all ${
                                belowFoldTab === cat.id
                                  ? 'bg-slate-900 text-white shadow-sm'
                                  : 'bg-white text-slate-600 border border-slate-200 hover:bg-slate-100'
                              }`}
                            >
                              {cat.label}
                            </button>
                          ))}
                        </div>
                      </div>

                      <div className="flex items-center gap-4 overflow-x-auto pb-4 no-scrollbar">
                        {LOCAL_PLACES.filter((p) => p.category === belowFoldTab).map((place) => (
                          <div
                            key={place.id}
                            className="w-[260px] shrink-0 bg-white rounded-2xl border border-slate-200 overflow-hidden shadow-md hover:shadow-xl transition-all group"
                          >
                            <div className="h-36 relative overflow-hidden">
                              <img
                                src={place.image}
                                alt={place.name}
                                className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
                              />
                              <span className="absolute top-2.5 left-2.5 bg-blue-600 text-white text-[10px] font-bold px-2 py-0.5 rounded-full">
                                {place.tag}
                              </span>
                            </div>

                            <div className="p-3.5 space-y-2">
                              <div className="flex items-center justify-between text-[11px]">
                                <span className="font-bold text-amber-500">⭐ {place.rating}</span>
                                <span className="text-slate-400">({place.reviews} รีวิว)</span>
                              </div>
                              <h4 className="font-bold text-xs text-slate-900 line-clamp-1">{place.name}</h4>
                              <p className="text-[10px] text-slate-500 line-clamp-2 leading-relaxed">{place.subtext}</p>
                              
                              <div className="pt-2 border-t border-slate-100 flex items-center justify-between">
                                <span className="text-xs font-extrabold text-blue-600">{place.price}</span>
                                <button
                                  onClick={() => addToTripCart(place)}
                                  className="px-3 py-1.5 rounded-lg bg-blue-50 hover:bg-blue-600 hover:text-white text-blue-600 text-[11px] font-bold transition-all"
                                >
                                  + ใส่ทริปนี้
                                </button>
                              </div>
                            </div>
                          </div>
                        ))}
                      </div>
                    </div>

                  </section>
                </div>
              )}

              {/* VIEW 2: ITINERARY SCHEDULE VIEW */}
              {currentView === 'itinerary' && (
                <div className="animate-in fade-in duration-200 p-4 lg:p-6 max-w-[1600px] mx-auto space-y-6">
                  
                  {/* ITINERARY HEADER ACTIONS */}
                  <div className="flex flex-col sm:flex-row sm:items-center justify-between gap-4 bg-white rounded-3xl p-5 border border-slate-200 shadow-xl shadow-slate-200/50">
                    <div className="flex items-center gap-3">
                      <button
                        onClick={() => setCurrentView('search')}
                        className="px-3.5 py-2 rounded-2xl bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold transition-all flex items-center gap-1.5 shrink-0"
                      >
                        <span>← กลับหน้าค้นหา</span>
                      </button>
                      <div>
                        <h1 className="text-lg lg:text-xl font-black text-slate-900 leading-tight">
                          ตารางแผนการเดินทาง: กรุงเทพฯ & เชียงใหม่ สมาร์ตทริป
                        </h1>
                        <p className="text-xs text-slate-500 mt-0.5">
                          {startDate} ถึง {endDate} • {adults + childrenCount} ผู้เดินทาง
                        </p>
                      </div>
                    </div>

                    <div className="flex items-center gap-2 self-end sm:self-auto">
                      <button
                        onClick={() => setIsShareModalOpen(true)}
                        className="px-3.5 py-2 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold transition-all flex items-center gap-1.5"
                      >
                        <span>🔗 แชร์ทริปนี้</span>
                      </button>
                      <button
                        onClick={() => triggerToast('ดาวน์โหลด PDF ตารางเดินทางเรียบร้อยแล้ว!')}
                        className="px-3.5 py-2 rounded-xl bg-blue-600 hover:bg-blue-700 text-white text-xs font-bold transition-all shadow-md shadow-blue-500/20 flex items-center gap-1.5"
                      >
                        <span>📥 ส่งออก PDF</span>
                      </button>
                    </div>
                  </div>

                  {/* BUDGET & SPLIT BILL CARD */}
                  <section className="bg-white rounded-3xl border border-slate-200/90 p-5 lg:p-6 shadow-xl shadow-slate-200/50 relative overflow-hidden">
                    <div className="grid grid-cols-1 lg:grid-cols-12 gap-6 items-center">
                      
                      {/* Spent vs Budget Progress Bar (7 Columns) */}
                      <div className="lg:col-span-7 space-y-3">
                        <div className="flex items-center justify-between">
                          <div>
                            <h2 className="text-sm sm:text-base font-extrabold text-slate-900 flex items-center gap-2">
                              <span>💰 สรุปงบประมาณ & ค่าใช้จ่ายจริง</span>
                              <span className="text-[11px] font-semibold px-2.5 py-0.5 rounded-full bg-blue-50 text-blue-700 border border-blue-200">
                                {spentPercentage}% ใช้ไปแล้ว
                              </span>
                            </h2>
                            <p className="text-xs text-slate-500 mt-0.5">
                              คำนวณจากกิจกรรมทั้งหมดในตารางทริป
                            </p>
                          </div>
                          <div className="text-right">
                            <span className="text-xs text-slate-400 block">งบตั้งไว้</span>
                            <span className="font-extrabold text-slate-800 text-sm">{overallBudget.toLocaleString()} ฿</span>
                          </div>
                        </div>

                        {/* Progress Bar */}
                        <div className="w-full bg-slate-100 rounded-full h-3 overflow-hidden p-0.5 border border-slate-200">
                          <div 
                            className={`h-full rounded-full transition-all duration-500 ${
                              spentPercentage > 90 ? 'bg-rose-500' : spentPercentage > 75 ? 'bg-amber-500' : 'bg-blue-600'
                            }`}
                            style={{ width: `${spentPercentage}%` }}
                          ></div>
                        </div>

                        <div className="flex items-center justify-between text-xs pt-1">
                          <span className="text-slate-600 font-medium">
                            ใช้ไปแล้ว: <strong className="text-blue-600 font-bold">{totalSpent.toLocaleString()} ฿</strong>
                          </span>
                          <span className="text-slate-600 font-medium">
                            คงเหลือ: <strong className={overallBudget - totalSpent < 0 ? 'text-rose-600 font-bold' : 'text-emerald-600 font-bold'}>
                              {(overallBudget - totalSpent).toLocaleString()} ฿
                            </strong>
                          </span>
                        </div>
                      </div>

                      {/* Split Bill Summary (5 Columns) */}
                      <div className="lg:col-span-5 bg-slate-50 rounded-2xl p-4 border border-slate-200 flex items-center justify-between gap-4">
                        <div>
                          <div className="text-xs font-bold text-slate-800 flex items-center gap-1.5">
                            <span>👥 หารค่าใช้จ่าย (Split Bill)</span>
                          </div>
                          <div className="text-[11px] text-slate-500 mt-0.5">
                            เฉลี่ยต่อคน ({travelerCount} คน)
                          </div>
                          <div className="text-lg font-black text-blue-600 mt-1">
                            ~{avgCostPerPerson.toLocaleString()} ฿ <span className="text-xs font-normal text-slate-500">/ คน</span>
                          </div>
                        </div>

                        <div className="flex items-center gap-2">
                          <div className="flex flex-col items-center">
                            <span className="text-[10px] text-slate-400 font-medium mb-1">จำนวนคน</span>
                            <div className="flex items-center gap-1.5 bg-white border border-slate-300 rounded-xl p-1 shadow-sm">
                              <button 
                                onClick={() => setTravelerCount(Math.max(1, travelerCount - 1))}
                                className="w-6 h-6 rounded-lg bg-slate-100 hover:bg-slate-200 font-bold text-xs flex items-center justify-center text-slate-700"
                              >
                                -
                              </button>
                              <span className="w-5 text-center font-bold text-xs text-slate-800">{travelerCount}</span>
                              <button 
                                onClick={() => setTravelerCount(travelerCount + 1)}
                                className="w-6 h-6 rounded-lg bg-slate-100 hover:bg-slate-200 font-bold text-xs flex items-center justify-center text-slate-700"
                              >
                                +
                              </button>
                            </div>
                          </div>
                        </div>
                      </div>

                    </div>
                  </section>

                  {/* DAYS SELECTOR TABS & DAY HEADER ACTIONS */}
                  <section className="space-y-4">
                    <div className="flex items-center justify-between flex-wrap gap-3">
                      {/* Day Selector Pills */}
                      <div className="flex items-center gap-2 overflow-x-auto pb-1 no-scrollbar">
                        {daysData.map((day, idx) => (
                          <button
                            key={day.id}
                            onClick={() => setActiveDayIdx(idx)}
                            className={`px-4 py-2.5 rounded-2xl text-xs font-bold transition-all shrink-0 flex items-center gap-2 ${
                              activeDayIdx === idx
                                ? 'bg-blue-600 text-white shadow-lg shadow-blue-500/25 border border-blue-500'
                                : 'bg-white text-slate-600 border border-slate-200 hover:bg-slate-100'
                            }`}
                          >
                            <span>{day.label}</span>
                            <span className={`text-[10px] px-2 py-0.5 rounded-full ${
                              activeDayIdx === idx ? 'bg-white/20 text-white' : 'bg-slate-100 text-slate-500'
                            }`}>
                              {day.activities.length} กิจกรรม
                            </span>
                          </button>
                        ))}

                        <button
                          onClick={() => {
                            const newDayNum = daysData.length + 1;
                            const newDay = {
                              id: `day${newDayNum}`,
                              label: `DAY ${newDayNum}`,
                              dateStr: `วันถัดไป`,
                              title: `วันกิจกรรมเพิ่มเติม`,
                              totalDist: '10.0 กม.',
                              totalTime: '30 นาที',
                              transportMode: '🚗 รถยนต์ส่วนตัว',
                              activities: []
                            };
                            setDaysData([...daysData, newDay]);
                            setActiveDayIdx(daysData.length);
                            triggerToast(`เพิ่ม DAY ${newDayNum} สำเร็จแล้ว!`);
                          }}
                          className="px-3.5 py-2.5 rounded-2xl bg-slate-100 hover:bg-slate-200 text-slate-700 text-xs font-bold border border-slate-300 transition-all flex items-center gap-1.5 shrink-0"
                        >
                          <span>+ เพิ่มวัน</span>
                        </button>
                      </div>

                      {/* Quick Day Actions */}
                      <div className="flex items-center gap-2">
                        <button
                          onClick={handleOptimizeRoute}
                          className="px-3.5 py-2 rounded-xl bg-gradient-to-r from-amber-500 to-orange-500 hover:from-amber-600 hover:to-orange-600 text-white text-xs font-bold flex items-center gap-1.5 shadow-md shadow-amber-500/20 transition-all active:scale-95"
                        >
                          <span>⚡ Optimize Route</span>
                        </button>
                        <button
                          onClick={() => setIsAddModalOpen(true)}
                          className="px-3.5 py-2 rounded-xl bg-emerald-600 hover:bg-emerald-700 text-white text-xs font-bold flex items-center gap-1.5 shadow-md shadow-emerald-600/20 transition-all active:scale-95"
                        >
                          <span>+ เพิ่มกิจกรรม</span>
                        </button>
                      </div>
                    </div>

                    {/* Active Day Meta Info Bar */}
                    <div className="bg-slate-900 text-white rounded-2xl p-4 flex flex-col sm:flex-row sm:items-center justify-between gap-3 border border-slate-800">
                      <div>
                        <div className="flex items-center gap-2 text-xs text-blue-400 font-semibold">
                          <span>{activeDay.dateStr}</span>
                          <span>•</span>
                          <span>{activeDay.transportMode}</span>
                        </div>
                        <h3 className="text-base font-bold text-white mt-0.5">{activeDay.title}</h3>
                      </div>
                      
                      <div className="flex items-center gap-4 text-xs text-slate-300 bg-slate-800/80 px-3.5 py-2 rounded-xl border border-slate-700">
                        <div className="flex items-center gap-1.5">
                          <span>📍</span>
                          <span>ระยะทางรวม: <strong className="text-white font-bold">{activeDay.totalDist}</strong></span>
                        </div>
                        <div className="w-[1px] h-4 bg-slate-700"></div>
                        <div className="flex items-center gap-1.5">
                          <span>⏱️</span>
                          <span>เวลาเดินทางรวม: <strong className="text-white font-bold">{activeDay.totalTime}</strong></span>
                        </div>
                      </div>
                    </div>
                  </section>

                  {/* ITINERARY MAIN CONTENT: TIMELINE LIST & ROUTE MAP */}
                  <section className="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
                    
                    {/* TIMELINE ACTIVITIES LIST (7 Cols) */}
                    <div className="lg:col-span-7 space-y-4">
                      {activeDay.activities.length === 0 ? (
                        <div className="bg-white rounded-3xl p-12 text-center border border-slate-200 text-slate-400 space-y-3">
                          <div className="text-4xl">🗓️</div>
                          <div className="font-bold text-sm text-slate-700">ยังไม่มีกิจกรรมในวันนี้</div>
                          <p className="text-xs">คลิกปุ่ม "+ เพิ่มกิจกรรม" เพื่อเริ่มจัดรายการในตาราง</p>
                        </div>
                      ) : (
                        activeDay.activities.map((act, idx) => (
                          <div key={act.id} className="space-y-3">
                            {/* Activity Item Card */}
                            <div className="bg-white rounded-2xl border border-slate-200 p-4 shadow-sm hover:shadow-md transition-all space-y-3 group relative">
                              <div className="flex items-start justify-between gap-3">
                                <div className="flex items-start gap-3">
                                  <span className="w-7 h-7 rounded-full bg-blue-600 text-white font-bold text-xs flex items-center justify-center shrink-0 mt-0.5 shadow-md shadow-blue-500/20">
                                    {idx + 1}
                                  </span>
                                  <div>
                                    <div className="flex items-center gap-2 flex-wrap">
                                      <span className="text-xs font-bold text-blue-600 bg-blue-50 px-2 py-0.5 rounded-md border border-blue-100">
                                        ⏰ {act.time}
                                      </span>
                                      <span className={`text-[10px] font-bold px-2 py-0.5 rounded-full border ${getCategoryBadgeClass(act.category)}`}>
                                        {act.category}
                                      </span>
                                    </div>
                                    <h4 className="font-bold text-sm text-slate-900 mt-1.5">{act.title}</h4>
                                  </div>
                                </div>

                                {/* Right Action Menu: Move up/down, Edit, Delete */}
                                <div className="flex items-center gap-1">
                                  <button
                                    onClick={() => handleMoveActivity(idx, 'up')}
                                    disabled={idx === 0}
                                    className="p-1.5 rounded-lg text-slate-400 hover:bg-slate-100 disabled:opacity-30 text-xs"
                                    title="เลื่อนขึ้น"
                                  >
                                    ⬆️
                                  </button>
                                  <button
                                    onClick={() => handleMoveActivity(idx, 'down')}
                                    disabled={idx === activeDay.activities.length - 1}
                                    className="p-1.5 rounded-lg text-slate-400 hover:bg-slate-100 disabled:opacity-30 text-xs"
                                    title="เลื่อนลง"
                                  >
                                    ⬇️
                                  </button>
                                  <button
                                    onClick={() => setEditingActivity(act)}
                                    className="p-1.5 rounded-lg text-slate-400 hover:text-blue-600 hover:bg-blue-50 text-xs"
                                    title="แก้ไข"
                                  >
                                    ✏️
                                  </button>
                                  <button
                                    onClick={() => handleDeleteActivity(act.id)}
                                    className="p-1.5 rounded-lg text-slate-400 hover:text-rose-600 hover:bg-rose-50 text-xs"
                                    title="ลบ"
                                  >
                                    🗑️
                                  </button>
                                </div>
                              </div>

                              {act.note && (
                                <div className="text-xs text-slate-500 bg-slate-50 p-2.5 rounded-xl border border-slate-100 flex items-center gap-1.5">
                                  <span>💡</span>
                                  <span>{act.note}</span>
                                </div>
                              )}

                              <div className="flex items-center justify-between text-xs pt-1 border-t border-slate-100">
                                <span className="text-slate-400">ค่าใช้จ่ายประมาณการ</span>
                                <span className="font-bold text-slate-800">{act.cost.toLocaleString()} THB</span>
                              </div>
                            </div>

                            {/* Travel Indicator line between activities */}
                            {act.travelNext && idx < activeDay.activities.length - 1 && (
                              <div className="flex items-center gap-3 px-6 text-[11px] text-slate-500 font-medium my-1">
                                <div className="w-0.5 h-6 bg-slate-300 ml-3"></div>
                                <span className="bg-slate-100 border border-slate-200 px-3 py-1 rounded-full text-slate-600">
                                  {act.travelNext}
                                </span>
                              </div>
                            )}
                          </div>
                        ))
                      )}
                    </div>

                    {/* ROUTE MAP CONTAINER (5 Cols) */}
                    <div className="lg:col-span-5 bg-white rounded-3xl border border-slate-200 p-4 shadow-xl shadow-slate-200/50 sticky top-20">
                      <div className="flex items-center justify-between mb-3 px-1">
                        <h3 className="font-bold text-xs text-slate-800 flex items-center gap-1.5">
                          <span>🗺️ เส้นทางเดินทางประจำวัน ({activeDay.label})</span>
                        </h3>
                        <span className="text-[10px] text-slate-400 bg-slate-100 px-2 py-0.5 rounded-md">
                          Interactive Route Map
                        </span>
                      </div>

                      {/* Map Canvas */}
                      <div className="bg-[#E2EAF4] rounded-2xl h-[420px] relative overflow-hidden border border-slate-200 shadow-inner">
                        <div className="absolute inset-0 opacity-20 pointer-events-none bg-[radial-gradient(#0066FF_1px,transparent_1px)] [background-size:16px_16px]"></div>
                        
                        {/* Route Lines SVG */}
                        <svg className="absolute inset-0 w-full h-full pointer-events-none stroke-blue-600 fill-none" viewBox="0 0 100 100" preserveAspectRatio="none">
                          <path
                            d={getSvgPath(activeDay.activities)}
                            strokeWidth="2"
                            strokeDasharray="3 3"
                            strokeLinecap="round"
                          />
                        </svg>

                        {/* Activity Pins on Map */}
                        {activeDay.activities.map((act, idx) => (
                          <div
                            key={act.id}
                            style={act.coords}
                            className="absolute -translate-x-1/2 -translate-y-1/2 group cursor-pointer z-10"
                          >
                            <div className="relative flex items-center justify-center">
                              <div className="w-7 h-7 rounded-full bg-blue-600 text-white font-black text-xs flex items-center justify-center shadow-lg border-2 border-white group-hover:scale-125 transition-transform">
                                {idx + 1}
                              </div>
                              {/* Tooltip Card */}
                              <div className="absolute bottom-8 left-1/2 -translate-x-1/2 bg-slate-900 text-white text-[10px] py-1 px-2.5 rounded-xl whitespace-nowrap shadow-xl opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none z-30">
                                <div className="font-bold">{act.title}</div>
                                <div className="text-blue-300">{act.time}</div>
                              </div>
                            </div>
                          </div>
                        ))}
                      </div>
                    </div>

                  </section>
                </div>
              )}

            </main>

          </div>

          {/* AUTO PLAN WIZARD MODAL (3-STEP SYSTEM) */}
          {isWizardOpen && (
            <div className="fixed inset-0 z-50 bg-slate-900/70 backdrop-blur-sm flex items-center justify-center p-4 animate-in fade-in duration-200">
              <div className="bg-white rounded-3xl max-w-xl w-full shadow-2xl overflow-hidden border border-slate-100 flex flex-col max-h-[90vh]">
                
                {/* Modal Header Banner */}
                <div className="bg-gradient-to-r from-[#0B192C] via-[#1E3A8A] to-[#0066FF] text-white p-5 flex items-start justify-between relative shrink-0">
                  <div>
                    <div className="flex items-center gap-2">
                      <span className="text-xl">⚡</span>
                      <h2 className="text-lg font-bold">Auto Plan Wizard</h2>
                    </div>
                    <p className="text-xs text-blue-200 mt-0.5">
                      ระบบช่วยประมวลผลจัดแผนท่องเที่ยวอัตโนมัติใน 3 ขั้นตอน
                    </p>
                  </div>
                  <button
                    onClick={() => setIsWizardOpen(false)}
                    className="w-8 h-8 rounded-full bg-white/10 hover:bg-white/20 text-white flex items-center justify-center text-sm transition-colors"
                  >
                    ✕
                  </button>
                </div>

                {/* TOP 3-STEP PROGRESS BAR */}
                <div className="bg-slate-100 px-5 py-3 border-b border-slate-200 flex items-center justify-between text-xs font-semibold shrink-0">
                  <div className={`flex items-center gap-1.5 ${wizardStep >= 1 ? 'text-blue-600 font-bold' : 'text-slate-400'}`}>
                    <span className={`w-5 h-5 rounded-full flex items-center justify-center text-[10px] ${wizardStep >= 1 ? 'bg-blue-600 text-white' : 'bg-slate-300'}`}>1</span>
                    <span>1. สไตล์ & การเดินทาง</span>
                  </div>
                  <span className="text-slate-300">➔</span>
                  
                  <div className={`flex items-center gap-1.5 ${wizardStep >= 2 ? 'text-blue-600 font-bold' : 'text-slate-400'}`}>
                    <span className={`w-5 h-5 rounded-full flex items-center justify-center text-[10px] ${wizardStep >= 2 ? 'bg-blue-600 text-white' : 'bg-slate-300'}`}>2</span>
                    <span>2. ที่พัก & งบประมาณ</span>
                  </div>
                  <span className="text-slate-300">➔</span>
                  
                  <div className={`flex items-center gap-1.5 ${wizardStep >= 3 ? 'text-blue-600 font-bold' : 'text-slate-400'}`}>
                    <span className={`w-5 h-5 rounded-full flex items-center justify-center text-[10px] ${wizardStep >= 3 ? 'bg-blue-600 text-white' : 'bg-slate-300'}`}>3</span>
                    <span>3. สรุปความต้องการ</span>
                  </div>
                </div>

                {/* MODAL BODY CONTENT */}
                <div className="p-6 overflow-y-auto space-y-5 flex-1">
                  
                  {/* STEP 1 */}
                  {wizardStep === 1 && (
                    <div className="space-y-5 animate-in fade-in duration-200">
                      <div className="font-bold text-sm text-slate-800 flex items-center gap-2 border-b border-slate-100 pb-2">
                        <span className="w-2.5 h-2.5 rounded-full bg-blue-600"></span>
                        <span>ขั้นตอนที่ 1: สไตล์การเที่ยว & การเดินทาง</span>
                      </div>

                      <div>
                        <label className="block text-xs font-bold text-slate-700 mb-2">
                          เลือกสไตล์การเที่ยวที่คุณชอบ (เลือกได้หลายข้อ):
                        </label>
                        <div className="grid grid-cols-2 gap-3">
                          {[
                            { id: 'ผ่อนคลาย', label: '☀️ ผ่อนคลาย' },
                            { id: 'ถ่ายรูป', label: '📸 ถ่ายรูป' },
                            { id: 'สายกิน', label: '🍜 สายกิน' },
                            { id: 'สายลุย', label: '🌲 สายลุย' },
                          ].map((item) => {
                            const checked = wizardStyles.includes(item.id);
                            return (
                              <label
                                key={item.id}
                                className={`p-3.5 rounded-2xl border-2 flex items-center gap-3 cursor-pointer text-xs font-semibold transition-all ${
                                  checked
                                    ? 'border-blue-600 bg-blue-50/60 text-blue-900 shadow-sm'
                                    : 'border-slate-200 hover:border-slate-300 text-slate-700 bg-slate-50/50'
                                }`}
                              >
                                <input
                                  type="checkbox"
                                  checked={checked}
                                  onChange={() => toggleWizardStyle(item.id)}
                                  className="w-4 h-4 text-blue-600 rounded focus:ring-blue-500 cursor-pointer"
                                />
                                <span>{item.label}</span>
                              </label>
                            );
                          })}
                        </div>
                      </div>

                      <div>
                        <label className="block text-xs font-bold text-slate-700 mb-1.5">
                          โหมดการเดินทางหลัก (Transport Mode):
                        </label>
                        <select
                          value={wizardTransport}
                          onChange={(e) => setWizardTransport(e.target.value)}
                          className="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-2.5 text-xs font-medium text-slate-800 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                        >
                          <option value="รถยนต์ส่วนตัว / เช่ารถ (เน้นความสะดวก)">🚗 รถยนต์ส่วนตัว / เช่ารถ (เน้นความสะดวก)</option>
                          <option value="รถสาธารณะ / รถไฟฟ้า / Grab (ประหยัดงบ)">🚌 รถสาธารณะ / รถไฟฟ้า / Grab (ประหยัดงบ)</option>
                          <option value="รถจักรยานยนต์ / เดินเท้า (เน้นคล่องตัว)">🛵 รถจักรยานยนต์ / เดินเท้า (เน้นคล่องตัว)</option>
                        </select>
                      </div>
                    </div>
                  )}

                  {/* STEP 2 */}
                  {wizardStep === 2 && (
                    <div className="space-y-5 animate-in fade-in duration-200">
                      <div className="font-bold text-sm text-slate-800 flex items-center gap-2 border-b border-slate-100 pb-2">
                        <span className="w-2.5 h-2.5 rounded-full bg-blue-600"></span>
                        <span>ขั้นตอนที่ 2: ที่พัก & งบประมาณห้องพัก</span>
                      </div>

                      <div className="space-y-3">
                        <label
                          className={`p-3.5 rounded-2xl border-2 block cursor-pointer text-xs transition-all ${
                            wizardAccOption === 'option1'
                              ? 'border-blue-600 bg-blue-50/50 shadow-sm'
                              : 'border-slate-200 hover:border-slate-300 bg-slate-50/30'
                          }`}
                        >
                          <div className="flex items-center gap-2.5 font-bold text-slate-800">
                            <input
                              type="radio"
                              name="accOpt"
                              checked={wizardAccOption === 'option1'}
                              onChange={() => setWizardAccOption('option1')}
                              className="w-4 h-4 text-blue-600 focus:ring-blue-500"
                            />
                            <span>1. จองที่พักผ่านระบบแล้ว (In-App Booking)</span>
                          </div>
                          <p className="text-[11px] text-slate-500 ml-6 mt-1">
                            ระบบจะนำตำแหน่งที่พักจากการจองในแอปมาจัดจุดท่องเที่ยวรอบๆ ให้โดยอัตโนมัติ
                          </p>
                        </label>

                        <label
                          className={`p-3.5 rounded-2xl border-2 block cursor-pointer text-xs transition-all ${
                            wizardAccOption === 'option2'
                              ? 'border-blue-600 bg-blue-50/50 shadow-sm'
                              : 'border-slate-200 hover:border-slate-300 bg-slate-50/30'
                          }`}
                        >
                          <div className="flex items-center gap-2.5 font-bold text-slate-800">
                            <input
                              type="radio"
                              name="accOpt"
                              checked={wizardAccOption === 'option2'}
                              onChange={() => setWizardAccOption('option2')}
                              className="w-4 h-4 text-blue-600 focus:ring-blue-500"
                            />
                            <span>2. มีที่พักแล้ว (จองข้างนอก / External)</span>
                          </div>

                          {wizardAccOption === 'option2' && (
                            <div className="ml-6 mt-3 space-y-2 pt-2 border-t border-slate-200/80 animate-in fade-in duration-150">
                              <div>
                                <label className="block text-[11px] font-semibold text-slate-700">ชื่อโรงแรมหรือย่านที่พัก:</label>
                                <input
                                  type="text"
                                  value={wizardAccName}
                                  onChange={(e) => setWizardAccName(e.target.value)}
                                  placeholder="เช่น โรงแรมศาลา อรุณ กรุงเทพฯ"
                                  className="w-full mt-1 bg-white border border-slate-300 rounded-xl px-3 py-2 text-xs focus:ring-2 focus:ring-blue-500 focus:outline-none"
                                />
                              </div>
                            </div>
                          )}
                        </label>

                        <label
                          className={`p-3.5 rounded-2xl border-2 block cursor-pointer text-xs transition-all ${
                            wizardAccOption === 'option3'
                              ? 'border-blue-600 bg-blue-50/50 shadow-sm'
                              : 'border-slate-200 hover:border-slate-300 bg-slate-50/30'
                          }`}
                        >
                          <div className="flex items-center gap-2.5 font-bold text-slate-800">
                            <input
                              type="radio"
                              name="accOpt"
                              checked={wizardAccOption === 'option3'}
                              onChange={() => setWizardAccOption('option3')}
                              className="w-4 h-4 text-blue-600 focus:ring-blue-500"
                            />
                            <span>3. ยังไม่มีที่พัก</span>
                          </div>

                          {wizardAccOption === 'option3' && (
                            <div className="ml-6 mt-3 p-3.5 bg-white rounded-xl border border-blue-200 space-y-3 animate-in fade-in duration-200">
                              <label className="block text-xs font-bold text-blue-900">
                                กำหนดงบประมาณค่าห้องพักที่คุณต้องการ (ระบุราคาต่อคืน)
                              </label>
                              
                              <div className="relative flex items-center">
                                <input
                                  type="number"
                                  min="0"
                                  step="100"
                                  value={wizardCustomHotelBudget}
                                  onChange={(e) => setWizardCustomHotelBudget(Number(e.target.value))}
                                  placeholder="เช่น 1,500"
                                  className="w-full bg-slate-50 border border-slate-300 rounded-xl pl-3.5 pr-16 py-2.5 text-sm font-bold text-slate-800 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                                />
                                <span className="absolute right-3.5 text-xs font-bold text-slate-500">
                                  ฿ / คืน
                                </span>
                              </div>

                              <div className="flex flex-wrap items-center gap-1.5 pt-1">
                                <span className="text-[10px] text-slate-400 font-medium">ราคาแนะนำ:</span>
                                {[1000, 1500, 2500, 4000, 6000].map((preset) => (
                                  <button
                                    key={preset}
                                    type="button"
                                    onClick={() => setWizardCustomHotelBudget(preset)}
                                    className={`px-2 py-0.5 rounded-lg text-[10px] font-semibold transition-all ${
                                      wizardCustomHotelBudget === preset
                                        ? 'bg-blue-600 text-white'
                                        : 'bg-slate-100 text-slate-600 hover:bg-slate-200'
                                    }`}
                                  >
                                    {preset.toLocaleString()} ฿
                                  </button>
                                ))}
                              </div>
                            </div>
                          )}
                        </label>
                      </div>
                    </div>
                  )}

                  {/* STEP 3 */}
                  {wizardStep === 3 && (
                    <div className="space-y-5 animate-in fade-in duration-200">
                      <div className="font-bold text-sm text-slate-800 flex items-center gap-2 border-b border-slate-100 pb-2">
                        <span className="w-2.5 h-2.5 rounded-full bg-emerald-500"></span>
                        <span>ขั้นตอนที่ 3: สรุปความต้องการ</span>
                      </div>

                      <div className="bg-slate-50 border border-slate-200 rounded-2xl p-4 space-y-3 text-xs">
                        <div className="font-bold text-slate-800 border-b border-slate-200 pb-2 flex items-center justify-between">
                          <span className="flex items-center gap-1.5">
                            <span>📋</span>
                            <span>รายละเอียดสำหรับประมวลผลทริป</span>
                          </span>
                          <span className="text-[10px] bg-emerald-100 text-emerald-800 px-2.5 py-0.5 rounded-full font-bold">
                            พร้อมสร้างแพลน
                          </span>
                        </div>

                        <div className="grid grid-cols-2 gap-3 text-slate-600">
                          <div>
                            <span className="font-semibold text-slate-800 block">จุดหมายปลายทาง:</span>
                            <span className="text-slate-700">{PROVINCES_DATA.find((p) => p.id === destination)?.name}</span>
                          </div>
                          <div>
                            <span className="font-semibold text-slate-800 block">วันเดินทาง:</span>
                            <span className="text-slate-700">{startDate} ถึง {endDate}</span>
                          </div>
                          <div>
                            <span className="font-semibold text-slate-800 block">งบรวมทั้งทริป:</span>
                            <span className="text-blue-600 font-bold">{totalBudget.toLocaleString()} THB</span>
                          </div>
                          <div>
                            <span className="font-semibold text-slate-800 block">จำนวนผู้เดินทาง:</span>
                            <span className="text-slate-700">ผู้ใหญ่ {adults} คน {childrenCount > 0 ? `, เด็ก ${childrenCount} คน` : ''}</span>
                          </div>
                          <div>
                            <span className="font-semibold text-slate-800 block">สไตล์การเที่ยว:</span>
                            <span className="text-slate-700">{wizardStyles.join(', ') || 'ทั่วไป'}</span>
                          </div>
                          <div>
                            <span className="font-semibold text-slate-800 block">โหมดการเดินทาง:</span>
                            <span className="text-slate-700">{wizardTransport}</span>
                          </div>
                        </div>

                        <div className="pt-2 border-t border-slate-200 text-[11px] text-slate-500">
                          🏡 <strong className="text-slate-700">สถานะที่พัก:</strong> {
                            wizardAccOption === 'option1' ? 'จองผ่านระบบแล้ว' :
                            wizardAccOption === 'option2' ? `มีที่พักแล้ว (${wizardAccName || 'ไม่ได้ระบุชื่อ'})` :
                            `ยังไม่มีที่พัก (งบประมาณ ${wizardCustomHotelBudget.toLocaleString()} ฿/คืน)`
                          }
                        </div>
                      </div>
                    </div>
                  )}

                </div>

                {/* MODAL FOOTER NAVIGATION */}
                <div className="p-4 bg-slate-50 border-t border-slate-200 flex items-center justify-between shrink-0">
                  {wizardStep > 1 ? (
                    <button
                      onClick={() => setWizardStep(wizardStep - 1)}
                      className="px-4 py-2 rounded-xl border border-slate-300 hover:bg-slate-200 text-slate-700 text-xs font-bold transition-all"
                    >
                      ← ย้อนกลับ
                    </button>
                  ) : (
                    <div></div>
                  )}

                  {wizardStep < 3 ? (
                    <button
                      onClick={() => setWizardStep(wizardStep + 1)}
                      className="px-5 py-2.5 rounded-xl bg-blue-600 hover:bg-blue-700 text-white text-xs font-bold transition-all shadow-md shadow-blue-500/20"
                    >
                      ถัดไป ➔
                    </button>
                  ) : (
                    <button
                      onClick={handleRunAutoWizardAnalysis}
                      disabled={isAnalyzing}
                      className="px-6 py-2.5 rounded-xl bg-gradient-to-r from-emerald-500 to-teal-600 hover:from-emerald-600 hover:to-teal-700 text-white text-xs font-extrabold transition-all shadow-lg shadow-emerald-500/25 flex items-center gap-2 disabled:opacity-50"
                    >
                      {isAnalyzing ? (
                        <>
                          <span className="animate-spin">🌀</span>
                          <span>กำลังประมวลผล...</span>
                        </>
                      ) : (
                        <>
                          <span>⚡ วิเคราะห์และสร้างแพลนทันที</span>
                        </>
                      )}
                    </button>
                  )}
                </div>

              </div>
            </div>
          )}

          {/* TRIP CART SLIDE-OVER DRAWER */}
          {isCartOpen && (
            <div className="fixed inset-0 z-50 overflow-hidden bg-slate-900/60 backdrop-blur-xs flex justify-end animate-in fade-in duration-200">
              <div className="bg-white w-full max-w-md h-full shadow-2xl flex flex-col border-l border-slate-200">
                <div className="p-4 bg-[#0B192C] text-white flex items-center justify-between">
                  <div className="flex items-center gap-2">
                    <span className="text-xl">🎒</span>
                    <div>
                      <h3 className="font-bold text-sm">ทริปของฉัน (My Trip Basket)</h3>
                      <p className="text-[10px] text-slate-400">รายการสถานที่ที่เลือกบันทึกไว้</p>
                    </div>
                  </div>
                  <button
                    onClick={() => setIsCartOpen(false)}
                    className="w-8 h-8 rounded-full bg-slate-800 hover:bg-slate-700 text-slate-300 flex items-center justify-center text-xs"
                  >
                    ✕
                  </button>
                </div>

                <div className="p-4 flex-1 overflow-y-auto space-y-3">
                  {tripCart.length === 0 ? (
                    <div className="text-center py-12 text-slate-400 space-y-2">
                      <div className="text-4xl">🗺️</div>
                      <p className="text-xs font-semibold">ยังไม่มีสถานที่ในทริปของคุณ</p>
                      <p className="text-[11px] text-slate-400">กดปุ่ม "+ ใส่ทริปนี้" จากหมุดหรือการ์ดสถานที่เพื่อบันทึก</p>
                    </div>
                  ) : (
                    tripCart.map((place) => (
                      <div key={place.id} className="bg-slate-50 border border-slate-200 rounded-2xl p-3 flex items-center gap-3 relative group">
                        <img src={place.image} alt={place.name} className="w-16 h-16 rounded-xl object-cover" />
                        <div className="flex-1 min-w-0">
                          <span className="text-[9px] bg-blue-100 text-blue-700 px-2 py-0.5 rounded-full font-bold">
                            {place.categoryName || place.category}
                          </span>
                          <h4 className="font-bold text-xs text-slate-800 truncate mt-1">{place.name}</h4>
                          <div className="text-xs font-extrabold text-blue-600 mt-0.5">{place.price}</div>
                        </div>
                        <button
                          onClick={() => removeFromTripCart(place.id)}
                          className="w-7 h-7 rounded-lg bg-rose-50 text-rose-600 hover:bg-rose-600 hover:text-white text-xs font-bold flex items-center justify-center transition-colors"
                          title="ลบ"
                        >
                          🗑️
                        </button>
                      </div>
                    ))
                  )}
                </div>

                <div className="p-4 bg-slate-50 border-t border-slate-200 space-y-3">
                  <div className="flex justify-between text-xs font-bold">
                    <span>สถานที่รวมทั้งหมด:</span>
                    <span className="text-blue-600">{tripCart.length} รายการ</span>
                  </div>
                  <button
                    onClick={() => {
                      setIsCartOpen(false);
                      setCurrentView('itinerary');
                      triggerToast('นำเข้าสถานที่สู่ตารางเดินทางเรียบร้อยแล้ว!');
                    }}
                    className="w-full py-3 rounded-xl bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-bold text-xs shadow-lg shadow-blue-500/25 transition-all"
                  >
                    ยืนยันและไปที่ตารางเดินทาง 🚀
                  </button>
                </div>
              </div>
            </div>
          )}

          {/* SIDEBAR SERVICE MODAL (HELPER TOOL) */}
          {activeToolModal && (
            <div className="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
              <div className="bg-white rounded-3xl max-w-md w-full p-6 shadow-2xl border border-slate-100 space-y-4 animate-in fade-in duration-200">
                <div className="flex items-center justify-between border-b border-slate-100 pb-3">
                  <div className="flex items-center gap-2">
                    <span className="text-2xl">{activeToolModal.icon}</span>
                    <h3 className="font-bold text-base text-slate-900">{activeToolModal.label}</h3>
                  </div>
                  <button
                    onClick={() => setActiveToolModal(null)}
                    className="w-7 h-7 rounded-full bg-slate-100 hover:bg-slate-200 text-slate-600 text-xs font-bold"
                  >
                    ✕
                  </button>
                </div>
                <p className="text-xs text-slate-600 leading-relaxed">
                  {activeToolModal.desc || 'บริการเสริมและเครื่องมืออำนวยความสะดวกสำหรับการเดินทางของคุณ'}
                </p>
                <div className="p-4 bg-blue-50 rounded-2xl border border-blue-100 text-xs text-blue-900">
                  💡 ระบบพร้อมเปิดใช้งานบริการในส่วนนี้ คุณสามารถค้นหา จอง หรือคำนวณข้อมูลได้ทันที
                </div>
                <button
                  onClick={() => setActiveToolModal(null)}
                  className="w-full py-2.5 rounded-xl bg-slate-900 text-white text-xs font-bold hover:bg-slate-800 transition-colors"
                >
                  ปิดหน้าต่างนี้
                </button>
              </div>
            </div>
          )}

          {/* EDIT ACTIVITY MODAL */}
          {editingActivity && (
            <div className="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
              <div className="bg-white rounded-3xl max-w-md w-full p-6 shadow-2xl space-y-4 animate-in fade-in duration-200">
                <div className="flex items-center justify-between border-b border-slate-100 pb-3">
                  <h3 className="font-bold text-sm text-slate-900">✏️ แก้ไขรายละเอียดกิจกรรม</h3>
                  <button onClick={() => setEditingActivity(null)} className="text-slate-400 hover:text-slate-600">✕</button>
                </div>

                <div className="space-y-3 text-xs">
                  <div>
                    <label className="block font-bold text-slate-700 mb-1">ชื่อกิจกรรม / สถานที่:</label>
                    <input
                      type="text"
                      value={editingActivity.title}
                      onChange={(e) => setEditingActivity({ ...editingActivity, title: e.target.value })}
                      className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                    />
                  </div>

                  <div className="grid grid-cols-2 gap-3">
                    <div>
                      <label className="block font-bold text-slate-700 mb-1">ช่วงเวลา:</label>
                      <input
                        type="text"
                        value={editingActivity.time}
                        onChange={(e) => setEditingActivity({ ...editingActivity, time: e.target.value })}
                        className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                      />
                    </div>
                    <div>
                      <label className="block font-bold text-slate-700 mb-1">ค่าใช้จ่าย (THB):</label>
                      <input
                        type="number"
                        value={editingActivity.cost}
                        onChange={(e) => setEditingActivity({ ...editingActivity, cost: Number(e.target.value) })}
                        className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                      />
                    </div>
                  </div>

                  <div>
                    <label className="block font-bold text-slate-700 mb-1">บันทึกเพิ่มเติม / คำแนะนำ:</label>
                    <input
                      type="text"
                      value={editingActivity.note || ''}
                      onChange={(e) => setEditingActivity({ ...editingActivity, note: e.target.value })}
                      className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                    />
                  </div>
                </div>

                <div className="flex items-center gap-2 pt-2">
                  <button
                    onClick={() => setEditingActivity(null)}
                    className="flex-1 py-2.5 rounded-xl border border-slate-300 text-slate-700 text-xs font-bold hover:bg-slate-100"
                  >
                    ยกเลิก
                  </button>
                  <button
                    onClick={handleSaveEditActivity}
                    className="flex-1 py-2.5 rounded-xl bg-blue-600 text-white text-xs font-bold hover:bg-blue-700 shadow-md shadow-blue-500/20"
                  >
                    บันทึกการแก้ไข
                  </button>
                </div>
              </div>
            </div>
          )}

          {/* ADD ACTIVITY MODAL */}
          {isAddModalOpen && (
            <div className="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
              <div className="bg-white rounded-3xl max-w-md w-full p-6 shadow-2xl space-y-4 animate-in fade-in duration-200">
                <div className="flex items-center justify-between border-b border-slate-100 pb-3">
                  <h3 className="font-bold text-sm text-slate-900">➕ เพิ่มกิจกรรมใหม่ลงใน {activeDay.label}</h3>
                  <button onClick={() => setIsAddModalOpen(false)} className="text-slate-400 hover:text-slate-600">✕</button>
                </div>

                <div className="space-y-3 text-xs">
                  <div>
                    <label className="block font-bold text-slate-700 mb-1">ชื่อกิจกรรม / สถานที่:</label>
                    <input
                      type="text"
                      value={newActivityTitle}
                      onChange={(e) => setNewActivityTitle(e.target.value)}
                      placeholder="เช่น ทานอาหารเย็น ร้านริมน้ำ"
                      className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                    />
                  </div>

                  <div className="grid grid-cols-2 gap-3">
                    <div>
                      <label className="block font-bold text-slate-700 mb-1">ช่วงเวลา:</label>
                      <input
                        type="text"
                        value={newActivityTime}
                        onChange={(e) => setNewActivityTime(e.target.value)}
                        placeholder="14:00 - 15:30"
                        className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                      />
                    </div>
                    <div>
                      <label className="block font-bold text-slate-700 mb-1">ประเภท:</label>
                      <select
                        value={newActivityCategory}
                        onChange={(e) => setNewActivityCategory(e.target.value)}
                        className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                      >
                        <option value="Attraction">สถานที่ท่องเที่ยว</option>
                        <option value="Cafe">คาเฟ่ & ร้านอาหาร</option>
                        <option value="Stay">ที่พักแนะนำ</option>
                        <option value="Souvenir">ของฝาก & ช้อปปิ้ง</option>
                      </select>
                    </div>
                  </div>

                  <div>
                    <label className="block font-bold text-slate-700 mb-1">ค่าใช้จ่ายประมาณการ (THB):</label>
                    <input
                      type="number"
                      value={newActivityCost}
                      onChange={(e) => setNewActivityCost(Number(e.target.value))}
                      className="w-full border border-slate-300 rounded-xl px-3 py-2 focus:ring-2 focus:ring-blue-500 focus:outline-none"
                    />
                  </div>
                </div>

                <div className="flex items-center gap-2 pt-2">
                  <button
                    onClick={() => setIsAddModalOpen(false)}
                    className="flex-1 py-2.5 rounded-xl border border-slate-300 text-slate-700 text-xs font-bold hover:bg-slate-100"
                  >
                    ยกเลิก
                  </button>
                  <button
                    onClick={handleAddActivity}
                    className="flex-1 py-2.5 rounded-xl bg-emerald-600 text-white text-xs font-bold hover:bg-emerald-700 shadow-md shadow-emerald-500/20"
                  >
                    + เพิ่มลงในตาราง
                  </button>
                </div>
              </div>
            </div>
          )}

          {/* SHARE TRIP MODAL */}
          {isShareModalOpen && (
            <div className="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-xs flex items-center justify-center p-4">
              <div className="bg-white rounded-3xl max-w-sm w-full p-6 shadow-2xl text-center space-y-4 animate-in fade-in duration-200">
                <div className="text-3xl">🔗</div>
                <h3 className="font-bold text-base text-slate-900">แชร์ตารางแผนการเดินทางนี้</h3>
                <p className="text-xs text-slate-500">คัดลอกลิงก์เพื่อส่งต่อให้เพื่อนร่วมทริปของคุณดูได้ทันที</p>
                <div className="p-3 bg-slate-100 rounded-xl text-xs text-slate-600 font-mono truncate select-all">
                  https://uplan.travel/share/trip-892341
                </div>
                <button
                  onClick={() => {
                    setIsShareModalOpen(false);
                    triggerToast('คัดลอกลิงก์เรียบร้อยแล้ว!');
                  }}
                  className="w-full py-2.5 rounded-xl bg-blue-600 text-white text-xs font-bold hover:bg-blue-700 transition-colors"
                >
                  คัดลอกลิงก์ชวนเพื่อน
                </button>
              </div>
            </div>
          )}

        </div>
      );
    }

    // Render React App to DOM
    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
  </script>
</body>
</html>
