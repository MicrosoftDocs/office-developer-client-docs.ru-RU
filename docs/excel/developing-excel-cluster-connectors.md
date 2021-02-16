---
title: Разработка соединители кластера Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412599"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="36ffd-103">Разработка соединители кластера Excel</span><span class="sxs-lookup"><span data-stu-id="36ffd-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="36ffd-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="36ffd-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="36ffd-105">Соединитель кластера Excel предоставляет средства для автоматической разгрузки кластерно-безопасных вызовов пользовательских функций в XLL на кластерный сервер.</span><span class="sxs-lookup"><span data-stu-id="36ffd-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="36ffd-106">Описание функций, безопасных для кластера, см. в описании [безопасных функций кластера.](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="36ffd-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="36ffd-107">Такая разгрузка может повысить производительность, позволяя использовать больше вычислительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36ffd-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="36ffd-108">Соединители кластера обычно разрабатываются поставщиком кластера высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="36ffd-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="36ffd-109">Соединители кластера</span><span class="sxs-lookup"><span data-stu-id="36ffd-109">Cluster Connectors</span></span>

<span data-ttu-id="36ffd-110">Соединитель кластера — это DLL,который предоставляет определенные точки входа, которые Excel использует для координации вызовов пользовательских функций, безопасных для кластера.</span><span class="sxs-lookup"><span data-stu-id="36ffd-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="36ffd-111">Он служит интерфейсом между Excel и высокоскоростным вычислительным кластером для управления сеансами, для выполнения вызовов функций (путем передачи полного имени функции и фактических аргументов вызова) и для возврата результатов вызова в Excel с помощью механизма обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="36ffd-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="36ffd-112">Чтобы создать соединитель кластера, создайте DLL-запись, которая предоставляет точки входа, перечисленные в функциях [соединители кластера Excel.](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="36ffd-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="36ffd-113">Установка кластерного соединителя</span><span class="sxs-lookup"><span data-stu-id="36ffd-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="36ffd-114">Чтобы сделать соединитель кластера доступным в Excel, код установки соединителя должен установить DLL соединителя на компьютер, на котором установлен Excel.</span><span class="sxs-lookup"><span data-stu-id="36ffd-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="36ffd-115">Кроме того, код установки соединителю должен добавить запись для соединителю в следующем ключе реестра:</span><span class="sxs-lookup"><span data-stu-id="36ffd-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="36ffd-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="36ffd-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span></span>\
  
<span data-ttu-id="36ffd-117">Добавьте узел в этот ключ для соединителю кластера, который указывает следующие строки:</span><span class="sxs-lookup"><span data-stu-id="36ffd-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="36ffd-118">`Name`— имя, которое будет отображаться в списке соединитений кластера в Excel.</span><span class="sxs-lookup"><span data-stu-id="36ffd-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="36ffd-119">`Filename`— полный путь для DLL.</span><span class="sxs-lookup"><span data-stu-id="36ffd-119">`Filename`—the full path for the DLL.</span></span>
    

