---
title: Действия макроса SetField (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Действие SetField используется для присвоения значения поля.
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807115"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="a246f-103">Действия макроса SetField (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="a246f-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="a246f-104">Действие **SetField** используется для присвоения значения поля.</span><span class="sxs-lookup"><span data-stu-id="a246f-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a246f-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a246f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a246f-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="a246f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a246f-107">**SetField** действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="a246f-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="a246f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a246f-108">Setting</span></span>

<span data-ttu-id="a246f-109">Действие **SetField** содержит аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a246f-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="a246f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a246f-110">**Argument name**</span></span>|<span data-ttu-id="a246f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a246f-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a246f-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="a246f-112">**Name**</span></span> <br/> |<span data-ttu-id="a246f-113">Строка, идентифицирующая поле.</span><span class="sxs-lookup"><span data-stu-id="a246f-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="a246f-114">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a246f-114">**Value**</span></span> <br/> |<span data-ttu-id="a246f-115">Выражение, которое задает значение, задаваемое в поле.</span><span class="sxs-lookup"><span data-stu-id="a246f-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a246f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a246f-116">Remarks</span></span>

<span data-ttu-id="a246f-117">Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block-access-custom-web-app.md)** или **[ИзменитьЗапись](editrecord-data-block-access-custom-web-app.md)** .</span><span class="sxs-lookup"><span data-stu-id="a246f-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

