---
title: Функция TimeFromParts (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Возвращает значение времени на основе указанного частей.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807120"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="b9742-103">Функция TimeFromParts (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="b9742-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="b9742-104">Возвращает значение времени на основе указанного частей.</span><span class="sxs-lookup"><span data-stu-id="b9742-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b9742-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="b9742-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="b9742-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="b9742-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b9742-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9742-107">Syntax</span></span>

 <span data-ttu-id="b9742-108">**TimeFromParts** (*Час*, *минута* *второй*)</span><span class="sxs-lookup"><span data-stu-id="b9742-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="b9742-109">Функция **TimeFromParts** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b9742-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b9742-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="b9742-110">**Argument name**</span></span>|<span data-ttu-id="b9742-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b9742-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b9742-112">*Час*</span><span class="sxs-lookup"><span data-stu-id="b9742-112">*Hour*</span></span>  <br/> |<span data-ttu-id="b9742-113">Выражение целое число, указывающее часов.</span><span class="sxs-lookup"><span data-stu-id="b9742-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="b9742-114">*Минуты*</span><span class="sxs-lookup"><span data-stu-id="b9742-114">*Minute*</span></span>  <br/> |<span data-ttu-id="b9742-115">Выражение целое число, указывающее минут.</span><span class="sxs-lookup"><span data-stu-id="b9742-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="b9742-116">*Секунды*</span><span class="sxs-lookup"><span data-stu-id="b9742-116">*Second*</span></span>  <br/> |<span data-ttu-id="b9742-117">Выражение целое число, указывающее секунд.</span><span class="sxs-lookup"><span data-stu-id="b9742-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9742-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b9742-118">See also</span></span>

 <span data-ttu-id="b9742-119">**TimeFromParts** возвращает значение полностью инициализированный времени.</span><span class="sxs-lookup"><span data-stu-id="b9742-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="b9742-120">Если недопустимые аргументы, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b9742-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="b9742-121">Если параметры имеют значение null, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="b9742-121">If any of the parameters are null, null is returned.</span></span> 
  

