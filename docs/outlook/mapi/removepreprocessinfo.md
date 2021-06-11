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
# <a name="removepreprocessinfo"></a><span data-ttu-id="5a082-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="5a082-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="5a082-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a082-105">Удаляет предварительные сведения, написанные функцией [preprocessMessage](preprocessmessage.md) из сообщения.</span><span class="sxs-lookup"><span data-stu-id="5a082-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a082-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5a082-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a082-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="5a082-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="5a082-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="5a082-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5a082-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="5a082-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="5a082-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="5a082-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5a082-111">Шпалер MAPI</span><span class="sxs-lookup"><span data-stu-id="5a082-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="5a082-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5a082-112">Parameters</span></span>

 <span data-ttu-id="5a082-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5a082-113">_lpMessage_</span></span>
  
> <span data-ttu-id="5a082-114">[in] Указатель на предварительное сообщение, из которого должна быть удалена информация.</span><span class="sxs-lookup"><span data-stu-id="5a082-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a082-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a082-115">Return value</span></span>

<span data-ttu-id="5a082-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a082-116">S_OK</span></span>
  
> <span data-ttu-id="5a082-117">Предварительная информация была успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="5a082-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a082-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a082-118">Remarks</span></span>

<span data-ttu-id="5a082-119">Spooler MAPI вызывает функцию на основе **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="5a082-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="5a082-120">Поставщик транспорта регистрирует функцию **RemovePreprocessInfo** одновременно с регистрацией параллельной функции **preprocessMessage** в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md)</span><span class="sxs-lookup"><span data-stu-id="5a082-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="5a082-121">Визуализация изображения, пригодная для передачи факса, является примером предварительной подготовки сведений, написанных функцией, определенной прототипом функции [PreprocessMessage.](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5a082-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="5a082-122">Spooler MAPI обычно вызывает функцию **RemovePreprocessInfo** после отправки сообщения, которое содержит предварительно отображленную информацию.</span><span class="sxs-lookup"><span data-stu-id="5a082-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

