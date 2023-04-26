---
authors: ["kokkos-team"]
categories: ["Kokkos", "HPX backend"]
title: "HPX now available as an experimental backend"
date: "2019-04-09"
description: ""
---

{{< paige/image
    alt=""
    breakpoints=false
    class="object-fit-cover rounded-4 shadow"
    densities=""
    fetchpriority="high"
    height="20rem"
    link=""
    loading="eager"
    maxheight=""
    maxwidth=""
    process=""
    sizes=""
    src="/images/kokkos-blog-post1.jpg"
    srcset=""
    title=""
    width="100%" >}}

We are pleased to announce that Kokkos now has an HPX backend thanks to the work of Mikael Simberg from CSCS. This backend is the first backend capable of providing Kokkos’ asynchronous semantics on CPUs. It is fully functional including the task graph API. If you have time try it out and let us know how it goes. The backend is available on Kokkos’ “develop” branch: https://github.com/kokkos/kokkos/tree/develop and will be part of the Kokkos 3.0 release in May.
