---
title: Синтаксический анализ функции (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Анализирует текстовое значение и возвращает значение указанного типа, используя язык и региональные параметры приложения.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807093"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="bda40-103">Синтаксический анализ функции (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="bda40-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="bda40-104">Анализирует текстовое значение и возвращает значение указанного типа, используя язык и региональные параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="bda40-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bda40-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="bda40-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="bda40-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="bda40-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bda40-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bda40-107">Syntax</span></span>

 <span data-ttu-id="bda40-108">**Синтаксический анализ** (*TextExpression*, *тип данных*)</span><span class="sxs-lookup"><span data-stu-id="bda40-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="bda40-109">Функция **анализа** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="bda40-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="bda40-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="bda40-110">**Argument name**</span></span>|<span data-ttu-id="bda40-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bda40-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bda40-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="bda40-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="bda40-113">Выражение текст, представляющий форматированное значение для разбора в указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="bda40-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="bda40-114">*Тип данных*</span><span class="sxs-lookup"><span data-stu-id="bda40-114">*DataType*</span></span>  <br/> |<span data-ttu-id="bda40-115">Литерал значение, представляющее тип данных, требуемый для результата.</span><span class="sxs-lookup"><span data-stu-id="bda40-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bda40-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="bda40-116">Remarks</span></span>

<span data-ttu-id="bda40-117">Использование **анализа** только для преобразования из строки в число типов и даты и времени.</span><span class="sxs-lookup"><span data-stu-id="bda40-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="bda40-118">Для преобразования типа общие используйте функцию **преобразования** .</span><span class="sxs-lookup"><span data-stu-id="bda40-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="bda40-119">Имейте в виду, что существует определенных производительности дополнительную нагрузку при анализе строковое значение.</span><span class="sxs-lookup"><span data-stu-id="bda40-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

