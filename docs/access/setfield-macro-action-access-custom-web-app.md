---
title: Макрокоманда SetField (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Действие SetField можно использовать для присвоения значения полю.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432928"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="4120d-103">Макрокоманда SetField (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="4120d-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="4120d-104">Действие **SetField** можно использовать для присвоения значения полю.</span><span class="sxs-lookup"><span data-stu-id="4120d-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4120d-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4120d-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4120d-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="4120d-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4120d-107">Действие **SetField** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="4120d-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4120d-108">Setting</span><span class="sxs-lookup"><span data-stu-id="4120d-108">Setting</span></span>

<span data-ttu-id="4120d-109">Макрокоманда **SetField** содержит аргументы, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4120d-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="4120d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="4120d-110">**Argument name**</span></span>|<span data-ttu-id="4120d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="4120d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4120d-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="4120d-112">**Name**</span></span> <br/> |<span data-ttu-id="4120d-113">Строка, определяющая поле.</span><span class="sxs-lookup"><span data-stu-id="4120d-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="4120d-114">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4120d-114">**Value**</span></span> <br/> |<span data-ttu-id="4120d-115">Выражение, задающее значение, присваиваемое полю.</span><span class="sxs-lookup"><span data-stu-id="4120d-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4120d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4120d-116">Remarks</span></span>

<span data-ttu-id="4120d-117">Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block-access-custom-web-app.md)** или **[ИзменитьЗапись](editrecord-data-block-access-custom-web-app.md)** .</span><span class="sxs-lookup"><span data-stu-id="4120d-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

