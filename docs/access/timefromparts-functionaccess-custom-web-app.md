---
title: Функция Тимефромпартс (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Возвращает значение времени на основе указанных частей.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304251"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="13618-103">Функция Тимефромпартс (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="13618-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="13618-104">Возвращает значение времени на основе указанных частей.</span><span class="sxs-lookup"><span data-stu-id="13618-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13618-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="13618-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="13618-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="13618-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13618-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13618-107">Syntax</span></span>

 <span data-ttu-id="13618-108">**Тимефромпартс** (*Час*, *минута*, *секунда*)</span><span class="sxs-lookup"><span data-stu-id="13618-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="13618-109">Функция **тимефромпартс** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="13618-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="13618-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="13618-110">**Argument name**</span></span>|<span data-ttu-id="13618-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13618-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="13618-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="13618-112">*Hour*</span></span>  <br/> |<span data-ttu-id="13618-113">Целочисленное выражение, задающее часы.</span><span class="sxs-lookup"><span data-stu-id="13618-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="13618-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="13618-114">*Minute*</span></span>  <br/> |<span data-ttu-id="13618-115">Целочисленное выражение, задающее минуты.</span><span class="sxs-lookup"><span data-stu-id="13618-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="13618-116">*Second*</span><span class="sxs-lookup"><span data-stu-id="13618-116">*Second*</span></span>  <br/> |<span data-ttu-id="13618-117">Целочисленное выражение, задающее секунды.</span><span class="sxs-lookup"><span data-stu-id="13618-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13618-118">См. также</span><span class="sxs-lookup"><span data-stu-id="13618-118">See also</span></span>

 <span data-ttu-id="13618-119">**Тимефромпартс** Возвращает полностью инициализированное значение времени.</span><span class="sxs-lookup"><span data-stu-id="13618-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="13618-120">Если аргументы недопустимы, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="13618-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="13618-121">Если какой-либо из параметров имеет значение null, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="13618-121">If any of the parameters are null, null is returned.</span></span> 
  

