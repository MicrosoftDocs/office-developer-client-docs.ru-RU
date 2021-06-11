---
title: Try_Parse Function (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Парсирует текстовое значение указанного типа данных в культуре приложения или возвращает Null, если преобразование не допустимо.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427530"
---
# <a name="try_parse-function-access-custom-web-app"></a><span data-ttu-id="36c27-103">Try_Parse Function (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="36c27-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="36c27-104">Парсирует текстовое значение указанного типа данных в культуре приложения или возвращает Null, если преобразование не допустимо.</span><span class="sxs-lookup"><span data-stu-id="36c27-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="36c27-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="36c27-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="36c27-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="36c27-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36c27-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36c27-107">Syntax</span></span>

 <span data-ttu-id="36c27-108">**Try_Parse** *(TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="36c27-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="36c27-109">Функция **Try_Parse** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="36c27-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="36c27-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="36c27-110">**Argument name**</span></span>|<span data-ttu-id="36c27-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36c27-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36c27-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="36c27-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="36c27-113">Текстовое выражение, представляющее отформатированные значения для анализа в указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="36c27-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="36c27-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="36c27-114">*DataType*</span></span>  <br/> |<span data-ttu-id="36c27-115">Тип данных, в который можно разрезать  *TextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="36c27-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36c27-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="36c27-116">Remarks</span></span>

<span data-ttu-id="36c27-117">Используйте **Try_Parse** только для преобразования из строки в дату/время и типы номеров.</span><span class="sxs-lookup"><span data-stu-id="36c27-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="36c27-118">Для преобразований общего типа продолжайте использовать **Convert**.</span><span class="sxs-lookup"><span data-stu-id="36c27-118">For general type conversions, continue to use **Convert**.</span></span> 
  

