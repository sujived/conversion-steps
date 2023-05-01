# conversion into next js

## step 1.

- create file in pages folder according to page-name.js

## step 2.

- paste this code in that page and change content according to that page

```
import Head from 'next/head';
import React from 'react';
import dynamic from 'next/dynamic';
const CommonBanner = dynamic(import('@/components/CommonBanner'));
const TwoLinks = dynamic(import('@/components/TwoLinks'));

const PageName = () => {
  return (
    <>
      <Head>
        <link
          rel="preload"
          as="image"
          href="/EMReact/LCPImage/bannerName.webp"
          type="image/webp"
        />
        <title></title>
        <meta name="description" content="" />
        <meta name="keywords" content="" />
        <link rel="canonical" href="" />
      </Head>
      <main style={{ overflowX: 'hidden' }}>
        <CommonBanner
          bgImg={'/EMReact/LCPImage/bannerName.webp'}
          heading={''}
          para={''}
        />
        <TwoLinks
          secondPage={'Services'}
          link2={'services.php'}
          thirdPage={''}
          link3={''}
          fourthPage={''}
        />
      </main>
      <style>{`
        .zubk {
          padding-bottom: 0px !important;
        }
        .collegue-service .card {
          height: 250px !important;
          max-height: 250px !important;
          border: 2px solid #fff !important;
          background-color: rgba(0, 0, 0, 0) !important;
        }
        .sub-serve-mag-up-apr {
          margin-top: 0px !important;
        }
        .sub-serve-mag-up-apr-2 {
          padding-bottom: 150px !important;
        }
        @media (max-width: 1024px) {
          .indus-btn-two-study-new {
            width: 60%;
          }
        }
        @media (max-width: 768px) {
          .indus-btn-two-study-new {
            width: 50%;
          }
        }
      `}</style>
    </>
  );
};

export default PageName;

```

## step 3.

- create folder in components folder according to page name and create components
- eg. page-name ->
- PNSectionC.jsx - copy content from outsourcing sectionC 
- PNSectionD.jsx - if video section is there then copy outsourcing section D otherwise copy sectionE

## step 4.

call this components in our page and import its dynamically
