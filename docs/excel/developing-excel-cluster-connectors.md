---
title: Разработка Excel соединители кластера
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
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="e4510-103">Разработка Excel соединители кластера</span><span class="sxs-lookup"><span data-stu-id="e4510-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="e4510-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e4510-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e4510-105">Excel кластерные соединители предоставляют средства для автоматической разгрузки вызовов функций, определенных пользователем с безопасностью кластера, в XLL на кластерный сервер.</span><span class="sxs-lookup"><span data-stu-id="e4510-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="e4510-106">Описание кластерных функций, определяемого пользователем, см. в Сейф [Cluster Сейф.](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="e4510-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="e4510-107">Это разгрузка может повысить производительность, позволяя использовать дополнительные вычислительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e4510-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="e4510-108">Соединителю кластера обычно разрабатывается поставщиком кластера высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="e4510-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="e4510-109">Соединители кластера</span><span class="sxs-lookup"><span data-stu-id="e4510-109">Cluster Connectors</span></span>

<span data-ttu-id="e4510-110">Соединитель кластера — это DLL, который предоставляет определенные точки входа, которые Excel для координации вызовов функций, определенных пользователем с безопасностью кластера.</span><span class="sxs-lookup"><span data-stu-id="e4510-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="e4510-111">Он служит интерфейсом между Excel и высокой производительностью вычислительного кластера для управления сеансами, для выполнения вызовов функций (путем передачи полностью квалифицированного имени функции и фактических аргументов вызова), а также для возврата результатов вызовов в Excel с помощью механизма обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e4510-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="e4510-112">Чтобы создать соединитель кластера, создайте DLL, который предоставляет точки входа, перечисленные [в Excel функций соединители кластера.](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="e4510-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="e4510-113">Установка соединителя кластера</span><span class="sxs-lookup"><span data-stu-id="e4510-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="e4510-114">Чтобы сделать соединитель кластера доступным в Excel, код установки соединителя должен установить DLL соединителя на компьютере, на котором Excel установлен.</span><span class="sxs-lookup"><span data-stu-id="e4510-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="e4510-115">Кроме того, код установки соединиттеля должен добавить запись для соединителю под следующим ключом реестра:</span><span class="sxs-lookup"><span data-stu-id="e4510-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="e4510-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="e4510-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span></span>\
  
<span data-ttu-id="e4510-117">Добавьте узел в этот ключ соединителю кластера, который указывает следующие строки:</span><span class="sxs-lookup"><span data-stu-id="e4510-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="e4510-118">`Name`— имя, которое появится в списке соединитений кластера в Excel.</span><span class="sxs-lookup"><span data-stu-id="e4510-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="e4510-119">`Filename`— полный путь для DLL.</span><span class="sxs-lookup"><span data-stu-id="e4510-119">`Filename`—the full path for the DLL.</span></span>
    

