---
title: Parse Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Проансирует текстовое значение и возвращает его значение в заданный тип с использованием культуры приложения.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411136"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="51c5a-103">Parse Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="51c5a-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="51c5a-104">Проансирует текстовое значение и возвращает его значение в заданный тип с использованием культуры приложения.</span><span class="sxs-lookup"><span data-stu-id="51c5a-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="51c5a-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="51c5a-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="51c5a-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="51c5a-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51c5a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51c5a-107">Syntax</span></span>

 <span data-ttu-id="51c5a-108">**Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="51c5a-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="51c5a-109">Функция **parse** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="51c5a-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="51c5a-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="51c5a-110">**Argument name**</span></span>|<span data-ttu-id="51c5a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51c5a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="51c5a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="51c5a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="51c5a-113">Текстовое выражение, представляющее отформатированные значения для анализа в указанном типе данных.</span><span class="sxs-lookup"><span data-stu-id="51c5a-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="51c5a-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="51c5a-114">*DataType*</span></span>  <br/> |<span data-ttu-id="51c5a-115">Литерал, представляющий тип данных, запрашиваемого для результата.</span><span class="sxs-lookup"><span data-stu-id="51c5a-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51c5a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="51c5a-116">Remarks</span></span>

<span data-ttu-id="51c5a-117">Используйте **parse** только для преобразования из строки в типы даты и времени и числа.</span><span class="sxs-lookup"><span data-stu-id="51c5a-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="51c5a-118">Для преобразования общего типа используйте функцию **Convert.**</span><span class="sxs-lookup"><span data-stu-id="51c5a-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="51c5a-119">Помните, что при разборе строковых значений существуют определенные накладные расходы на производительность.</span><span class="sxs-lookup"><span data-stu-id="51c5a-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

