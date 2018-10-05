---
title: Функция Format (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Возвращает значение, отформатированное в соответствии с указанному шаблону.
ms.openlocfilehash: 1739f87fd6e77c91aa66a64c0b7520fa6a641e95
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387799"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="13645-103">Функция Format (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="13645-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="13645-104">Возвращает значение, отформатированное в соответствии с указанному шаблону.</span><span class="sxs-lookup"><span data-stu-id="13645-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13645-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="13645-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="13645-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="13645-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13645-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13645-107">Syntax</span></span>

 <span data-ttu-id="13645-108">**Формат** (*Выражение*, *Формат*)</span><span class="sxs-lookup"><span data-stu-id="13645-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="13645-109">Функция **Format** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="13645-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="13645-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="13645-110">**Argument name**</span></span>|<span data-ttu-id="13645-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13645-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="13645-112">*Выражение*</span><span class="sxs-lookup"><span data-stu-id="13645-112">*Expression*</span></span>  <br/> |<span data-ttu-id="13645-113">Выражение поддерживаемый тип данных для форматирования.</span><span class="sxs-lookup"><span data-stu-id="13645-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="13645-114">*Формат*</span><span class="sxs-lookup"><span data-stu-id="13645-114">*Format*</span></span>  <br/> | <span data-ttu-id="13645-115">Шаблон формата.</span><span class="sxs-lookup"><span data-stu-id="13645-115">A format pattern.</span></span> <span data-ttu-id="13645-116">Аргумент format должен содержать строку допустимый формат, как строка стандартного формата (например, «C» или «D») или образец настраиваемых символов для дат и числовых значений (например, «мммм дд, гггг (dddd)»).</span><span class="sxs-lookup"><span data-stu-id="13645-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="13645-117">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="13645-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13645-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="13645-118">Remarks</span></span>

<span data-ttu-id="13645-119">Для параметра *Format* вы можете передать строк, соответствующих любой из следующих шаблонов:</span><span class="sxs-lookup"><span data-stu-id="13645-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="13645-120">Строки стандартного числового формата</span><span class="sxs-lookup"><span data-stu-id="13645-120">Standard Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="13645-121">Строки настраиваемых числовых форматов</span><span class="sxs-lookup"><span data-stu-id="13645-121">Custom Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="13645-122">Стандартный формат даты и времени форматирования строк</span><span class="sxs-lookup"><span data-stu-id="13645-122">Standard Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="13645-123">Настраиваемые даты и времени форматирования строк</span><span class="sxs-lookup"><span data-stu-id="13645-123">Custom Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="13645-124">Функция **Format** нельзя использовать в следующих областях веб-приложений Access 2013:</span><span class="sxs-lookup"><span data-stu-id="13645-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="13645-125">Вычисляемых столбцов на уровне таблицы</span><span class="sxs-lookup"><span data-stu-id="13645-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="13645-126">Макросы пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="13645-126">UI macros</span></span>
    
- <span data-ttu-id="13645-127">Выражения в представлениях (например, в формах)</span><span class="sxs-lookup"><span data-stu-id="13645-127">Expressions in views (for example, in forms)</span></span>
    

