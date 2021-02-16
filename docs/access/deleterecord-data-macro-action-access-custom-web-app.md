---
title: Макрокод DeleteRecord Data Macro (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Для удаления записи можно использовать действие DeleteRecord.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423155"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="f5765-103">Макрокод DeleteRecord Data Macro (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="f5765-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="f5765-104">Для удаления **записи можно использовать действие DeleteRecord.**</span><span class="sxs-lookup"><span data-stu-id="f5765-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f5765-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f5765-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="f5765-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="f5765-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f5765-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="f5765-107">Setting</span></span>

<span data-ttu-id="f5765-108">Действие **DeleteRecord** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="f5765-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="f5765-109">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="f5765-109">**Argument**</span></span>|<span data-ttu-id="f5765-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5765-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5765-111">**Запись псевдонима**</span><span class="sxs-lookup"><span data-stu-id="f5765-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="f5765-112">Строка, идентифицирует запись, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f5765-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="f5765-113">Если  *аргумент Alias*  не указан, текущая запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="f5765-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5765-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f5765-114">Remarks</span></span>

<span data-ttu-id="f5765-115">Локализованную переменную **LastCreateRecordIdentity** можно использовать для работы с последней записью, созданной в блоке данных **CreateRecord.**</span><span class="sxs-lookup"><span data-stu-id="f5765-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="f5765-116">Например, используйте следующий синтаксис для ссылки на недавно созданную запись:</span><span class="sxs-lookup"><span data-stu-id="f5765-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


