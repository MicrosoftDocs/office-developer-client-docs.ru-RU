---
title: Функция TimeFromParts (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Возвращает значение времени на основе указанных частей.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417996"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="eb172-103">Функция TimeFromParts (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="eb172-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="eb172-104">Возвращает значение времени на основе указанных частей.</span><span class="sxs-lookup"><span data-stu-id="eb172-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="eb172-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="eb172-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="eb172-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="eb172-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eb172-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb172-107">Syntax</span></span>

 <span data-ttu-id="eb172-108">**TimeFromParts** *(час,* *минута,* *секунда)*</span><span class="sxs-lookup"><span data-stu-id="eb172-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="eb172-109">Функция **TimeFromParts** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="eb172-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="eb172-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="eb172-110">**Argument name**</span></span>|<span data-ttu-id="eb172-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb172-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eb172-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="eb172-112">*Hour*</span></span>  <br/> |<span data-ttu-id="eb172-113">Integer expression specifying hours.</span><span class="sxs-lookup"><span data-stu-id="eb172-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="eb172-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="eb172-114">*Minute*</span></span>  <br/> |<span data-ttu-id="eb172-115">Integer expression specifying minutes.</span><span class="sxs-lookup"><span data-stu-id="eb172-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="eb172-116">*Second*</span><span class="sxs-lookup"><span data-stu-id="eb172-116">*Second*</span></span>  <br/> |<span data-ttu-id="eb172-117">Integer expression specifying seconds.</span><span class="sxs-lookup"><span data-stu-id="eb172-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb172-118">См. также</span><span class="sxs-lookup"><span data-stu-id="eb172-118">See also</span></span>

 <span data-ttu-id="eb172-119">**TimeFromParts** возвращает полностью инициализированное значение времени.</span><span class="sxs-lookup"><span data-stu-id="eb172-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="eb172-120">Если аргументы недействительны, то вызывается ошибка.</span><span class="sxs-lookup"><span data-stu-id="eb172-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="eb172-121">Если любой из параметров является null, null возвращается.</span><span class="sxs-lookup"><span data-stu-id="eb172-121">If any of the parameters are null, null is returned.</span></span> 
  

