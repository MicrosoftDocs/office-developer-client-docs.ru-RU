---
title: Функция Try_Convert (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Преобразует значение указанного типа данных или возвращает значение Null, если преобразования не является допустимым.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807149"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="8f849-103">Функция Try_Convert (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="8f849-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="8f849-104">Преобразует значение указанного типа данных или возвращает значение Null, если преобразования не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="8f849-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8f849-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8f849-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="8f849-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="8f849-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8f849-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f849-107">Syntax</span></span>

 <span data-ttu-id="8f849-108">**Try_Convert** (*Тип данных*, *выражение*)</span><span class="sxs-lookup"><span data-stu-id="8f849-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="8f849-109">Функция **Try_Convert** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8f849-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8f849-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="8f849-110">**Argument name**</span></span>|<span data-ttu-id="8f849-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f849-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8f849-112">*Тип данных*</span><span class="sxs-lookup"><span data-stu-id="8f849-112">*DataType*</span></span>  <br/> |<span data-ttu-id="8f849-113">Тип данных, в котором для преобразования *выражения* .</span><span class="sxs-lookup"><span data-stu-id="8f849-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="8f849-114">*Выражение*</span><span class="sxs-lookup"><span data-stu-id="8f849-114">*Expression*</span></span>  <br/> |<span data-ttu-id="8f849-115">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8f849-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f849-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f849-116">Remarks</span></span>

 <span data-ttu-id="8f849-117">**Try_Convert** принимает значение, переданное в нее и пытается преобразовать его для указанного *типа данных* .</span><span class="sxs-lookup"><span data-stu-id="8f849-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="8f849-118">Если преобразование завершается успешно, **Try_Convert** возвращает значение как указанный *тип данных* ; Если возникает ошибка, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="8f849-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="8f849-119">Однако при запросе преобразования, явно не разрешено **Try_Convert** сбой с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8f849-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

