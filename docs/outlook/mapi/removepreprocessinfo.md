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
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812149"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="41ef2-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="41ef2-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="41ef2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41ef2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41ef2-105">Удаляет предварительно данные, записанные функцией [PreprocessMessage](preprocessmessage.md) на основе из сообщения.</span><span class="sxs-lookup"><span data-stu-id="41ef2-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41ef2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="41ef2-106">Header file:</span></span>  <br/> |<span data-ttu-id="41ef2-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="41ef2-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="41ef2-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="41ef2-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="41ef2-109">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="41ef2-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="41ef2-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="41ef2-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="41ef2-111">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="41ef2-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="41ef2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="41ef2-112">Parameters</span></span>

 <span data-ttu-id="41ef2-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="41ef2-113">_lpMessage_</span></span>
  
> <span data-ttu-id="41ef2-114">[in] Указатель на предварительной обработки сообщений, из которой должна быть удалены сведения.</span><span class="sxs-lookup"><span data-stu-id="41ef2-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41ef2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="41ef2-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="41ef2-116">S_OK</span></span>
  
> <span data-ttu-id="41ef2-117">Сведения о предварительной обработки был удален.</span><span class="sxs-lookup"><span data-stu-id="41ef2-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41ef2-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="41ef2-118">Remarks</span></span>

<span data-ttu-id="41ef2-119">Диспетчер очереди MAPI вызывает функцию на основании **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="41ef2-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="41ef2-120">Функция **RemovePreprocessInfo** на основе регистрирует поставщика транспорта в то же время, он регистрирует параллельный **PreprocessMessage** на основе функции при вызове метода [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="41ef2-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="41ef2-121">Изображение отображения подходит для передачи факса приведен пример записи функцией, определенные в прототип функции [PreprocessMessage](preprocessmessage.md)предварительной обработки данных.</span><span class="sxs-lookup"><span data-stu-id="41ef2-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="41ef2-122">Диспетчер очереди MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения, содержащее сведения о предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="41ef2-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

