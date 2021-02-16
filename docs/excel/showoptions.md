---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407699"
---
# <a name="showoptions"></a><span data-ttu-id="a5836-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="a5836-103">ShowOptions</span></span>

<span data-ttu-id="a5836-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5836-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5836-105">Отображает модальные диалоговые окна для сбора сведений от пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5836-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="a5836-106">Эта точка входа вызвана, когда пользователь нажимает кнопку "Параметры" рядом с полем типа кластера  для выбранного  соединитела кластера в диалоговом окне "Параметры **Excel"** (в категории "Дополнительные" в разделе "Формулы").  </span><span class="sxs-lookup"><span data-stu-id="a5836-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="a5836-107">Соединители кластера отвечают за реализацию собственного диалогового интерфейса параметров и хранение связанных данных в реестре или другом месте.</span><span class="sxs-lookup"><span data-stu-id="a5836-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="a5836-108">Параметры являются внутренними для соединители кластера.</span><span class="sxs-lookup"><span data-stu-id="a5836-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="a5836-109">Excel не знает о них.</span><span class="sxs-lookup"><span data-stu-id="a5836-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="a5836-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5836-110">Parameters</span></span>

<span data-ttu-id="a5836-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="a5836-111">_hWndParent_</span></span>
  
> <span data-ttu-id="a5836-112">Окне Excel.</span><span class="sxs-lookup"><span data-stu-id="a5836-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5836-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5836-113">Return value</span></span>

<span data-ttu-id="a5836-114">**xlHpcRetSuccess,** если было показано диалоговое окно; **xlHpcRetCallFailed,** если он не был показан.</span><span class="sxs-lookup"><span data-stu-id="a5836-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a5836-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5836-115">Remarks</span></span>

<span data-ttu-id="a5836-116">Соединители кластера могут использовать это диалоговое окно для получения сведений, например о том, какой сервер кластера использовать, от пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5836-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5836-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a5836-117">See also</span></span>

- [<span data-ttu-id="a5836-118">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="a5836-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

