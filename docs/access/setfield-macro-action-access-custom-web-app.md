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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307899"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="23455-103">Макрокоманда SetField (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="23455-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="23455-104">Действие **SetField** можно использовать для присвоения значения полю.</span><span class="sxs-lookup"><span data-stu-id="23455-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="23455-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="23455-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="23455-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="23455-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="23455-107">Действие **SetField** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="23455-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="23455-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="23455-108">Setting</span></span>

<span data-ttu-id="23455-109">Макрокоманда **SetField** содержит аргументы, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="23455-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="23455-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="23455-110">**Argument name**</span></span>|<span data-ttu-id="23455-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="23455-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23455-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="23455-112">**Name**</span></span> <br/> |<span data-ttu-id="23455-113">Строка, определяющая поле.</span><span class="sxs-lookup"><span data-stu-id="23455-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="23455-114">**Значение**</span><span class="sxs-lookup"><span data-stu-id="23455-114">**Value**</span></span> <br/> |<span data-ttu-id="23455-115">Выражение, задающее значение, присваиваемое полю.</span><span class="sxs-lookup"><span data-stu-id="23455-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23455-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="23455-116">Remarks</span></span>

<span data-ttu-id="23455-117">Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block-access-custom-web-app.md)** или **[ИзменитьЗапись](editrecord-data-block-access-custom-web-app.md)** .</span><span class="sxs-lookup"><span data-stu-id="23455-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

