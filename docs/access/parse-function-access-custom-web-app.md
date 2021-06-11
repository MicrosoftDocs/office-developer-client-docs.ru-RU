---
title: Функция parse (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Parses a text value and returns its value in a given type using the culture of the application.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411136"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="4cdeb-103">Функция parse (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="4cdeb-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="4cdeb-104">Parses a text value and returns its value in a given type using the culture of the application.</span><span class="sxs-lookup"><span data-stu-id="4cdeb-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4cdeb-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="4cdeb-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="4cdeb-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="4cdeb-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4cdeb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cdeb-107">Syntax</span></span>

 <span data-ttu-id="4cdeb-108">**Parse** *(TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="4cdeb-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="4cdeb-109">Функция **Parse** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4cdeb-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="4cdeb-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="4cdeb-110">**Argument name**</span></span>|<span data-ttu-id="4cdeb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4cdeb-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4cdeb-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="4cdeb-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="4cdeb-113">Текстовое выражение, представляющее отформатированные значения для анализа в указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="4cdeb-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="4cdeb-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="4cdeb-114">*DataType*</span></span>  <br/> |<span data-ttu-id="4cdeb-115">Буквальное значение, представляющее тип данных, запрашиваемого для результата.</span><span class="sxs-lookup"><span data-stu-id="4cdeb-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cdeb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cdeb-116">Remarks</span></span>

<span data-ttu-id="4cdeb-117">Используйте **Parse** только для преобразования из строки в дату и время и типы номеров.</span><span class="sxs-lookup"><span data-stu-id="4cdeb-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="4cdeb-118">Для преобразований общего типа используйте функцию **Convert.**</span><span class="sxs-lookup"><span data-stu-id="4cdeb-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="4cdeb-119">Имейте в виду, что существует определенная накладная часть производительности при разборе значения строки.</span><span class="sxs-lookup"><span data-stu-id="4cdeb-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

