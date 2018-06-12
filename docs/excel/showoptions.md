---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807322"
---
# <a name="showoptions"></a><span data-ttu-id="a736c-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="a736c-103">ShowOptions</span></span>

<span data-ttu-id="a736c-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a736c-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a736c-105">Показывает модального диалогового окна для сбора сведений у пользователя.</span><span class="sxs-lookup"><span data-stu-id="a736c-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="a736c-106">Эта точка входа вызывается, когда пользователь нажимает кнопку **Параметры** рядом с полем **тип кластера** для соединителя выбранного кластера в диалоговом окне **Параметры Excel** (в категории **Дополнительно** в разделе **формулы** ).</span><span class="sxs-lookup"><span data-stu-id="a736c-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="a736c-107">Соединителей кластеров отвечают для реализации интерфейса диалогового окна собственные параметры, а также для хранения связанных данных в реестре или в другом месте.</span><span class="sxs-lookup"><span data-stu-id="a736c-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="a736c-108">Параметры являются внутренними относительно соединитель кластера.</span><span class="sxs-lookup"><span data-stu-id="a736c-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="a736c-109">Excel не знать о них.</span><span class="sxs-lookup"><span data-stu-id="a736c-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="a736c-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="a736c-110">Parameters</span></span>

<span data-ttu-id="a736c-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="a736c-111">_hWndParent_</span></span>
  
> <span data-ttu-id="a736c-112">Дескриптор окна Excel.</span><span class="sxs-lookup"><span data-stu-id="a736c-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a736c-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a736c-113">Return value</span></span>

<span data-ttu-id="a736c-114">**xlHpcRetSuccess** Если было показано диалоговое окно; **xlHpcRetCallFailed** , если он не отображается.</span><span class="sxs-lookup"><span data-stu-id="a736c-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a736c-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a736c-115">Remarks</span></span>

<span data-ttu-id="a736c-116">Соединителей кластеров можно использовать это диалоговое окно для получения информации, например какие кластера-сервера, у пользователя.</span><span class="sxs-lookup"><span data-stu-id="a736c-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a736c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a736c-117">See also</span></span>

- [<span data-ttu-id="a736c-118">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="a736c-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

