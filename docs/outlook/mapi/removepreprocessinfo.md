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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328380"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="a8be7-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="a8be7-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="a8be7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8be7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8be7-105">Удаляет предварительно обработанные сведения, записанные функцией на основе [препроцессмессаже](preprocessmessage.md) , из сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8be7-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8be7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a8be7-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8be7-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="a8be7-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a8be7-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a8be7-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a8be7-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="a8be7-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="a8be7-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="a8be7-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a8be7-111">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="a8be7-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="a8be7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8be7-112">Parameters</span></span>

 <span data-ttu-id="a8be7-113">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="a8be7-113">_lpMessage_</span></span>
  
> <span data-ttu-id="a8be7-114">возврата Указатель на предварительно обработанное сообщение, из которого удаляются сведения.</span><span class="sxs-lookup"><span data-stu-id="a8be7-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8be7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8be7-115">Return value</span></span>

<span data-ttu-id="a8be7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8be7-116">S_OK</span></span>
  
> <span data-ttu-id="a8be7-117">Предварительная обработка данных успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="a8be7-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8be7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8be7-118">Remarks</span></span>

<span data-ttu-id="a8be7-119">Диспетчер очереди MAPI вызывает функцию на основе **ремовепрепроцессинфо**.</span><span class="sxs-lookup"><span data-stu-id="a8be7-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="a8be7-120">Поставщик транспорта регистрирует функцию **ремовепрепроцессинфо** в то же время, когда она регистрирует параллельную функцию **препроцессмессаже** в вызове метода [имаписуппорт:: регистерпрепроцессор](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="a8be7-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="a8be7-121">Визуализация изображений, подходящая для передачи факсов, это пример предварительно обработанной информации, записанной функцией, определенной прототипом функции [препроцессмессаже](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="a8be7-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="a8be7-122">Диспетчер очереди MAPI обычно вызывает функцию **ремовепрепроцессинфо** после отправки сообщения, которое содержит предварительно обработанные сведения.</span><span class="sxs-lookup"><span data-stu-id="a8be7-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

