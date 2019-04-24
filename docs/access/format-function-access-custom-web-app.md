---
title: Функция Format (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Возвращает значение, отформатированное в соответствии с указанным шаблоном.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308206"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="9eee7-103">Функция Format (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="9eee7-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="9eee7-104">Возвращает значение, отформатированное в соответствии с указанным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="9eee7-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9eee7-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="9eee7-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="9eee7-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="9eee7-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9eee7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9eee7-107">Syntax</span></span>

 <span data-ttu-id="9eee7-108">**Format** (*Expression*, *Format*)</span><span class="sxs-lookup"><span data-stu-id="9eee7-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="9eee7-109">Функция **Format** включает в себя указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="9eee7-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="9eee7-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="9eee7-110">**Argument name**</span></span>|<span data-ttu-id="9eee7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9eee7-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9eee7-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="9eee7-112">*Expression*</span></span>  <br/> |<span data-ttu-id="9eee7-113">Выражение поддерживаемого типа данных, которое предназначено для форматирования.</span><span class="sxs-lookup"><span data-stu-id="9eee7-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="9eee7-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="9eee7-114">*Format*</span></span>  <br/> | <span data-ttu-id="9eee7-115">Шаблон форматирования.</span><span class="sxs-lookup"><span data-stu-id="9eee7-115">A format pattern.</span></span> <span data-ttu-id="9eee7-116">Аргумент Format должен содержать допустимую строку формата либо в виде строки стандартного формата (например, "C" или "D"), либо в виде шаблона пользовательских символов для дат и числовых значений (например, "ММММ дд, гггг (дддд)").</span><span class="sxs-lookup"><span data-stu-id="9eee7-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="9eee7-117">Дополнительные сведения см. в разделе "Комментарии".</span><span class="sxs-lookup"><span data-stu-id="9eee7-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9eee7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9eee7-118">Remarks</span></span>

<span data-ttu-id="9eee7-119">Для параметра *Format* можно передавать строки, соответствующие любому из указанных ниже шаблонов.</span><span class="sxs-lookup"><span data-stu-id="9eee7-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- <span data-ttu-id="9eee7-120">[Строки стандартного числового формата](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9eee7-120">[Standard Numeric Format Strings](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)</span></span>
    
- <span data-ttu-id="9eee7-121">[Строки пользовательского числового формата](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9eee7-121">[Custom Numeric Format Strings](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)</span></span>
    
- <span data-ttu-id="9eee7-122">[Строки стандартного формата даты и времени](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9eee7-122">[Standard Date and Time Format Strings](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)</span></span>
    
- <span data-ttu-id="9eee7-123">[Строки пользовательского формата даты и времени](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9eee7-123">[Custom Date and Time Format Strings](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)</span></span>
    
<span data-ttu-id="9eee7-124">Функция **Format** недоступна в следующих областях веб-приложений Access 2013:</span><span class="sxs-lookup"><span data-stu-id="9eee7-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="9eee7-125">вычисляемые столбцы на уровне таблицы;</span><span class="sxs-lookup"><span data-stu-id="9eee7-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="9eee7-126">макросы пользовательского интерфейса;</span><span class="sxs-lookup"><span data-stu-id="9eee7-126">UI macros</span></span>
    
- <span data-ttu-id="9eee7-127">выражения в представлениях (например, в формах).</span><span class="sxs-lookup"><span data-stu-id="9eee7-127">Expressions in views (for example, in forms)</span></span>
    

