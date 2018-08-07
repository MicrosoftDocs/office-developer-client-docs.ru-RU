---
title: Разработка соединителей кластеров Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807140"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="d5f16-103">Разработка соединителей кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="d5f16-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="d5f16-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d5f16-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d5f16-105">Соединителей кластеров для Excel предоставляют средства для автоматически разгрузки вызовов кластера safe пользовательской функции в надстройке XLL объединенных в кластер сервера.</span><span class="sxs-lookup"><span data-stu-id="d5f16-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="d5f16-106">Описание безопасного кластера пользовательских функций в разделе [Безопасные для кластера функции](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d5f16-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="d5f16-107">В этом разгрузки могут улучшить производительность, включив дополнительные вычислительные ресурсы для использования.</span><span class="sxs-lookup"><span data-stu-id="d5f16-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="d5f16-108">Соединитель кластера, как правило, разработанного поставщиком высокой производительности compute cluster.</span><span class="sxs-lookup"><span data-stu-id="d5f16-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="d5f16-109">Соединители кластера</span><span class="sxs-lookup"><span data-stu-id="d5f16-109">Cluster Connectors</span></span>

<span data-ttu-id="d5f16-110">Соединитель кластера — библиотеки DLL, которая предоставляет определенные точки входа, Excel использует для координации звонки кластера safe пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="d5f16-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="d5f16-111">Он выступает в качестве интерфейса между Excel и высокой производительности кластера для сеанса управления предъявления функция вызывает (путем передачи функция полное имя и фактических аргументов вызова) и возвращать результаты вызова в Excel через механизм обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d5f16-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="d5f16-112">Чтобы создать соединитель кластера, создайте библиотеку DLL, которая предоставляет точки входа, перечисленные в [Функции соединителя кластера Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d5f16-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="d5f16-113">Установка соединитель кластера</span><span class="sxs-lookup"><span data-stu-id="d5f16-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="d5f16-114">Соединитель кластера доступны в Excel, код настройки соединителя, необходимо установить библиотеку DLL соединителя на компьютере, где установлен Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d5f16-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="d5f16-115">Кроме того код настройки соединителя, необходимо добавить запись для соединителя в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="d5f16-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="d5f16-116">Connectors\ HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel кластера</span><span class="sxs-lookup"><span data-stu-id="d5f16-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="d5f16-117">Добавьте узел в этот раздел для соединителя кластера, который задает следующие строки:</span><span class="sxs-lookup"><span data-stu-id="d5f16-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="d5f16-118">`Name`— имя, которое будет отображаться в списке соединителей кластеров для Excel.</span><span class="sxs-lookup"><span data-stu-id="d5f16-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="d5f16-119">`Filename`— Полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="d5f16-119">`Filename`—the full path for the DLL.</span></span>
    

