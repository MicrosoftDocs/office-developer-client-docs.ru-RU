---
title: Функция Try_Parse (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Анализирует текстовое значение для указанного типа данных в языке и региональных параметрах приложения или возвращает значение Null, если преобразования не является допустимым.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807133"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="79176-103">Функция Try_Parse (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="79176-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="79176-104">Анализирует текстовое значение для указанного типа данных в языке и региональных параметрах приложения или возвращает значение Null, если преобразования не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="79176-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="79176-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="79176-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="79176-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="79176-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="79176-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79176-107">Syntax</span></span>

 <span data-ttu-id="79176-108">**Try_Parse** (*TextExpression*, *тип данных*)</span><span class="sxs-lookup"><span data-stu-id="79176-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="79176-109">Функция **Try_Parse** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="79176-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="79176-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="79176-110">**Argument name**</span></span>|<span data-ttu-id="79176-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="79176-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="79176-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="79176-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="79176-113">Выражение текст, представляющий форматированное значение для разбора в указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="79176-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="79176-114">*Тип данных*</span><span class="sxs-lookup"><span data-stu-id="79176-114">*DataType*</span></span>  <br/> |<span data-ttu-id="79176-115">Тип данных, в который необходимо проанализировать *TextExpression* .</span><span class="sxs-lookup"><span data-stu-id="79176-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79176-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="79176-116">Remarks</span></span>

<span data-ttu-id="79176-117">Используйте **Try_Parse** только для преобразования из строки в число типов и даты и времени.</span><span class="sxs-lookup"><span data-stu-id="79176-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="79176-118">Для преобразования общие типа продолжайте использовать **Преобразование**.</span><span class="sxs-lookup"><span data-stu-id="79176-118">For general type conversions, continue to use **Convert**.</span></span> 
  

