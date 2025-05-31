# Bhart_News
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const newsData = [
  {
    title: "भारत ने चंद्रयान-4 की तैयारी शुरू की",
    category: "टेक्नोलॉजी",
    summary: "ISRO ने चंद्रयान-4 मिशन के लिए परीक्षण शुरू कर दिए हैं, जो 2026 में लॉन्च हो सकता है।",
  },
  {
    title: "लोकसभा चुनाव 2024: अंतिम चरण का मतदान कल",
    category: "राजनीति",
    summary: "देशभर में 8 राज्यों की 57 सीटों पर मतदान होगा, प्रधानमंत्री ने की अपील।",
  },
  {
    title: "टीम इंडिया ने पाकिस्तान को हराया",
    category: "खेल",
    summary: "टी-20 वर्ल्ड कप में भारत ने पाकिस्तान को 7 विकेट से हराया।",
  },
];

export default function BharatNews() {
  return (
    <div className="p-4 max-w-4xl mx-auto">
      <h1 className="text-4xl font-bold text-center mb-6">🇮🇳 Bharat News</h1>

      <nav className="flex justify-center gap-4 mb-6 flex-wrap">
        {[
          "देश-विदेश",
          "राजनीति",
          "खेल",
          "मनोरंजन",
          "टेक्नोलॉजी",
          "शिक्षा",
        ].map((cat) => (
          <Button key={cat} variant="outline" className="text-sm">
            {cat}
          </Button>
        ))}
      </nav>

      <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
        {newsData.map((news, index) => (
          <Card key={index}>
            <CardContent className="p-4">
              <p className="text-sm text-muted-foreground mb-1">{news.category}</p>
              <h2 className="text-xl font-semibold mb-2">{news.title}</h2>
              <p className="text-sm text-gray-700">{news.summary}</p>
            </CardContent>
          </Card>
        ))}
      </div>

      <footer className="mt-10 text-center text-xs text-muted-foreground">
        © 2025 Bharat News. सभी अधिकार सुरक्षित।
      </footer>
    </div>
  );
}
