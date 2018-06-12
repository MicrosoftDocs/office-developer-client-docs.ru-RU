---
title: Функции обновления (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Возвращает попытка ли операция INSERT или UPDATE для указанного поля.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807144"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="7b727-103">Функции обновления (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="7b727-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="7b727-104">Возвращает попытка ли операция INSERT или UPDATE для указанного поля.</span><span class="sxs-lookup"><span data-stu-id="7b727-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7b727-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="7b727-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="7b727-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="7b727-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7b727-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b727-107">Syntax</span></span>

 <span data-ttu-id="7b727-108">**Обновление** (*Столбец*)</span><span class="sxs-lookup"><span data-stu-id="7b727-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="7b727-109">Функция **обновления** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="7b727-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="7b727-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="7b727-110">**Argument name**</span></span>|<span data-ttu-id="7b727-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b727-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7b727-112">*Столбец*</span><span class="sxs-lookup"><span data-stu-id="7b727-112">*Column*</span></span>  <br/> |<span data-ttu-id="7b727-113">Имя поля для проверки для операций вставки и обновления.</span><span class="sxs-lookup"><span data-stu-id="7b727-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b727-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b727-114">Remarks</span></span>

<span data-ttu-id="7b727-115">Функция **обновления** возвращает TRUE, независимо от того, при попытке вставки или обновления успешна.</span><span class="sxs-lookup"><span data-stu-id="7b727-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

