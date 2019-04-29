---
title: Разработка соединителей кластеров Excel
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
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="98120-103">Разработка соединителей кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="98120-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="98120-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98120-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98120-105">Кластерные соединители Excel предоставляют средства для автоматической разгрузки вызовов пользовательских функций, защищенных с помощью кластера, в XLL на кластерный сервер.</span><span class="sxs-lookup"><span data-stu-id="98120-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="98120-106">Описание функций, которые можно получить от кластера, можно найти в статье [безопасные функции кластера](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="98120-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="98120-107">Такая разгрузка может повысить производительность, позволяя использовать дополнительные вычислительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="98120-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="98120-108">Кластерный соединитель обычно разрабатывается с помощью высокопроизводительного вычислительного поставщика вычислительных кластеров.</span><span class="sxs-lookup"><span data-stu-id="98120-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="98120-109">Соединители кластера</span><span class="sxs-lookup"><span data-stu-id="98120-109">Cluster Connectors</span></span>

<span data-ttu-id="98120-110">Соединитель кластера — это библиотека DLL, которая предоставляет определенные точки входа, которые Excel использует для координирования вызовов пользовательских функций, не совместимых с кластером.</span><span class="sxs-lookup"><span data-stu-id="98120-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="98120-111">Он выступает в роли интерфейса между Excel и высокопроизводительным вычислительным кластером, для управления сеансами, для выполнения вызовов функций (путем передачи полных имен функций и фактических аргументов вызова), а также для возврата результатов вызова в Excel через механизм обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="98120-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="98120-112">Чтобы создать соединитель кластера, создайте БИБЛИОТЕКУ DLL, которая предоставляет точки входа, перечисленные в [функциях соединителя кластера Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="98120-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="98120-113">Установка соединителя кластера</span><span class="sxs-lookup"><span data-stu-id="98120-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="98120-114">Чтобы сделать соединитель кластера доступным в Excel, код установки соединителя должен установить DLL соединителя на компьютере, на котором установлено приложение Excel.</span><span class="sxs-lookup"><span data-stu-id="98120-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="98120-115">Кроме того, код установки соединителя должен добавить запись для соединителя в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="98120-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="98120-116">Соединители кластеров Хкэй_локал_мачине\софтваре\микрософт\оффице\ексцел\ексцел</span><span class="sxs-lookup"><span data-stu-id="98120-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="98120-117">Добавьте в этот раздел узел для соединителя кластера, указывающего следующие строки:</span><span class="sxs-lookup"><span data-stu-id="98120-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="98120-118">`Name`— имя, которое будет отображаться в списке соединителей кластера в Excel.</span><span class="sxs-lookup"><span data-stu-id="98120-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="98120-119">`Filename`— полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="98120-119">`Filename`—the full path for the DLL.</span></span>
    

