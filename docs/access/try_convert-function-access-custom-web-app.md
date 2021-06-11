---
title: Try_Convert Function (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Преобразует значение в указанный тип данных или возвращает Null, если преобразование не допустимо.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410898"
---
# <a name="try_convert-function-access-custom-web-app"></a><span data-ttu-id="e7669-103">Try_Convert Function (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="e7669-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="e7669-104">Преобразует значение в указанный тип данных или возвращает Null, если преобразование не допустимо.</span><span class="sxs-lookup"><span data-stu-id="e7669-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e7669-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e7669-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="e7669-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="e7669-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e7669-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7669-107">Syntax</span></span>

 <span data-ttu-id="e7669-108">**Try_Convert** *(DataType*, *Expression*)</span><span class="sxs-lookup"><span data-stu-id="e7669-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="e7669-109">Функция **Try_Convert** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e7669-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e7669-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="e7669-110">**Argument name**</span></span>|<span data-ttu-id="e7669-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e7669-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e7669-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="e7669-112">*DataType*</span></span>  <br/> |<span data-ttu-id="e7669-113">Тип данных, в который необходимо преобразовать *Expression.*</span><span class="sxs-lookup"><span data-stu-id="e7669-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="e7669-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="e7669-114">*Expression*</span></span>  <br/> |<span data-ttu-id="e7669-115">Значение, необходимое для преобразования.</span><span class="sxs-lookup"><span data-stu-id="e7669-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7669-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7669-116">Remarks</span></span>

 <span data-ttu-id="e7669-117">**Try_Convert** принимает переданные ему значения и пытается преобразовать его в указанный *DataType.*</span><span class="sxs-lookup"><span data-stu-id="e7669-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="e7669-118">Если преобразование успешно, **Try_Convert** возвращает значение в качестве указанного  *DataType;*  если возникает ошибка, возвращается null.</span><span class="sxs-lookup"><span data-stu-id="e7669-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="e7669-119">Однако если вы запросили преобразование, которое  явно не разрешено, Try_Convert с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e7669-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

