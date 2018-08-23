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
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588834"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="13820-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="13820-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="13820-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13820-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13820-105">Удаляет предварительно данные, записанные функцией [PreprocessMessage](preprocessmessage.md) на основе из сообщения.</span><span class="sxs-lookup"><span data-stu-id="13820-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13820-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="13820-106">Header file:</span></span>  <br/> |<span data-ttu-id="13820-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="13820-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="13820-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="13820-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="13820-109">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="13820-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="13820-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="13820-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="13820-111">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="13820-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="13820-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="13820-112">Parameters</span></span>

 <span data-ttu-id="13820-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="13820-113">_lpMessage_</span></span>
  
> <span data-ttu-id="13820-114">[in] Указатель на предварительной обработки сообщений, из которой должна быть удалены сведения.</span><span class="sxs-lookup"><span data-stu-id="13820-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13820-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="13820-115">Return value</span></span>

<span data-ttu-id="13820-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="13820-116">S_OK</span></span>
  
> <span data-ttu-id="13820-117">Сведения о предварительной обработки был удален.</span><span class="sxs-lookup"><span data-stu-id="13820-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13820-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="13820-118">Remarks</span></span>

<span data-ttu-id="13820-119">Диспетчер очереди MAPI вызывает функцию на основании **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="13820-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="13820-120">Функция **RemovePreprocessInfo** на основе регистрирует поставщика транспорта в то же время, он регистрирует параллельный **PreprocessMessage** на основе функции при вызове метода [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="13820-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="13820-121">Изображение отображения подходит для передачи факса приведен пример записи функцией, определенные в прототип функции [PreprocessMessage](preprocessmessage.md)предварительной обработки данных.</span><span class="sxs-lookup"><span data-stu-id="13820-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="13820-122">Диспетчер очереди MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения, содержащее сведения о предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="13820-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

