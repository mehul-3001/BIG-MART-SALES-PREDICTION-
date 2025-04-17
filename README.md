registry.addMapping("/**")
                .allowedOrigins("http://localhost:3000") // your frontend domain
                .allowedMethods("GET", "POST", "PUT", "DELETE", "OPTIONS")
                .allowedHeaders("*")
                .allowCredentials(true);


# BIG-MART-SALES-PREDICTION-
This is a ML model to predict the output sales.
## Group Member Details
Mehul Bokdia             - RA1911032010043 

Tadikonda Vinay          - RA1911032010044 

Vutukuri Noha            - RA1911032010046 

Yanala Venkat            - RA1911032010060 



const interpolateColor = (progress: number): string => {
  let r, g, b;

  if (progress <= 30) {
    // Yellow (0–30%)
    const ratio = progress / 30;
    r = 255;
    g = Math.floor(255 - ratio * 51);    // 255 → 204
    b = Math.floor(153 - ratio * 153);   // 153 → 0
  } else if (progress <= 40) {
    // Yellowish Orange (31–40%)
    const ratio = (progress - 30) / 10;
    r = 255;
    g = Math.floor(204 - ratio * 24);    // 204 → 180
    b = 0;
  } else if (progress <= 50) {
    // Orange (41–50%)
    const ratio = (progress - 40) / 10;
    r = 255;
    g = Math.floor(180 - ratio * 40);    // 180 → 140
    b = 0;
  } else if (progress <= 75) {
    // Greenish Orange (51–75%)
    const ratio = (progress - 50) / 25;
    r = Math.floor(255 - ratio * 75);    // 255 → 180
    g = Math.floor(140 + ratio * 60);    // 140 → 200
    b = 0;
  } else {
    // Green (76–100%)
    const ratio = (progress - 75) / 25;
    r = Math.floor(180 - ratio * 180);   // 180 → 0
    g = Math.floor(200 - ratio * 72);    // 200 → 128
    b = 0;
  }

  return `rgb(${r}, ${g}, ${b})`;
};
