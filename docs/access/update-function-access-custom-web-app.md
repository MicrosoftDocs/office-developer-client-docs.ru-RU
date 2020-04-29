---
title: Функция Update (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Возвращает значение, указывающее, была ли предпринята попытка выполнить операцию INSERT или UPDATE для указанного поля.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410919"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="a6cfb-103">Функция Update (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="a6cfb-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="a6cfb-104">Возвращает значение, указывающее, была ли предпринята попытка выполнить операцию INSERT или UPDATE для указанного поля.</span><span class="sxs-lookup"><span data-stu-id="a6cfb-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a6cfb-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="a6cfb-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="a6cfb-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a6cfb-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a6cfb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6cfb-107">Syntax</span></span>

 <span data-ttu-id="a6cfb-108">**Обновление** (*столбец*)</span><span class="sxs-lookup"><span data-stu-id="a6cfb-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="a6cfb-109">Функция **Update** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="a6cfb-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a6cfb-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a6cfb-110">**Argument name**</span></span>|<span data-ttu-id="a6cfb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a6cfb-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a6cfb-112">*Столбец*</span><span class="sxs-lookup"><span data-stu-id="a6cfb-112">*Column*</span></span>  <br/> |<span data-ttu-id="a6cfb-113">Имя поля, для которого проверяется операция вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="a6cfb-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6cfb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6cfb-114">Remarks</span></span>

<span data-ttu-id="a6cfb-115">Функция **Update** возвращает значение true независимо от того, успешно ли выполнена попытка вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="a6cfb-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

