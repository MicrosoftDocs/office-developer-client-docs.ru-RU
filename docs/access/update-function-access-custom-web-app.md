---
title: Функция обновления (доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Возвращает, была ли предпринята попытка операции INSERT или UPDATE на указанном поле.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410919"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="61f4f-103">Функция обновления (доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="61f4f-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="61f4f-104">Возвращает, была ли предпринята попытка операции INSERT или UPDATE на указанном поле.</span><span class="sxs-lookup"><span data-stu-id="61f4f-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61f4f-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="61f4f-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="61f4f-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="61f4f-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61f4f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61f4f-107">Syntax</span></span>

 <span data-ttu-id="61f4f-108">**Обновление** *(Столбец)*</span><span class="sxs-lookup"><span data-stu-id="61f4f-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="61f4f-109">Функция **Update** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="61f4f-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="61f4f-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="61f4f-110">**Argument name**</span></span>|<span data-ttu-id="61f4f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="61f4f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="61f4f-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="61f4f-112">*Column*</span></span>  <br/> |<span data-ttu-id="61f4f-113">Имя поля для проверки операции INSERT или UPDATE.</span><span class="sxs-lookup"><span data-stu-id="61f4f-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61f4f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="61f4f-114">Remarks</span></span>

<span data-ttu-id="61f4f-115">Функция **Update** возвращает TRUE независимо от успешной попытки INSERT или UPDATE.</span><span class="sxs-lookup"><span data-stu-id="61f4f-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

