
# Table of Contents

1.  [React Routing Quickstart](#org125b618)


<a id="org125b618"></a>

# React Routing Quickstart

    using react-router-dom

-   start inside App.jsx

    import { BrowserRouter, Routes, Route } from "react-router-dom";
    
    // App.jsx
    return (<>
            <BrowserRouter>
              <Routes>
                <Route path="/" element={<Layout />}> // base layout for every page
                  <Route index element={<Component />} /> // index page component
                  <Route path="backtest" element={<Component />} /> // different page component
                </Route>
              </Routes>
            </BrowserRouter>
            </>)

-   base layout

    // Layout.jsx
    export const Layout = () => {
            return (
                <>
                  <NavBar/>
                  <Outlet/>  // content for layout
                  <Footer/>
                </>
            )
        };

