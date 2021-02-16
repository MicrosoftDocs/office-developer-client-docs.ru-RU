---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432949"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="ed5d7-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="ed5d7-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="ed5d7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed5d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed5d7-105">Удаляет предварительно запроцесснутую информацию, написанную функцией на основе [PreprocessMessage,](preprocessmessage.md) из сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed5d7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ed5d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed5d7-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ed5d7-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ed5d7-108">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="ed5d7-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="ed5d7-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="ed5d7-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="ed5d7-110">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="ed5d7-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="ed5d7-111">MapI spooler</span><span class="sxs-lookup"><span data-stu-id="ed5d7-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ed5d7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed5d7-112">Parameters</span></span>

 <span data-ttu-id="ed5d7-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ed5d7-113">_lpMessage_</span></span>
  
> <span data-ttu-id="ed5d7-114">[in] Указатель на предварительное сообщение, из которого следует удалить информацию.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed5d7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed5d7-115">Return value</span></span>

<span data-ttu-id="ed5d7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed5d7-116">S_OK</span></span>
  
> <span data-ttu-id="ed5d7-117">Предварительно обучаемая информация была успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed5d7-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed5d7-118">Remarks</span></span>

<span data-ttu-id="ed5d7-119">Пулер MAPI вызывает функцию на основе **RemovePreprocessInfo.**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="ed5d7-120">Поставщик транспорта регистрирует функцию на основе **RemovePreprocessInfo** одновременно с регистрацией параллельной функции на основе **PreprocessMessage** в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md)</span><span class="sxs-lookup"><span data-stu-id="ed5d7-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="ed5d7-121">Отрисовка изображения, подходящая для передачи факсов, является примером предварительной подготовки информации, написанной функцией, определенной прототипом функции [PreprocessMessage.](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="ed5d7-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="ed5d7-122">Пулер MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения с предварительной подготовкой информации.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

