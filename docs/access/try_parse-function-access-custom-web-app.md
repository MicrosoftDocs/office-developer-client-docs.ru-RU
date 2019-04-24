---
title: Функция Три_парсе (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Выполняет синтаксический анализ текстового значения до указанного типа данных в культуре приложения или возвращает значение null, если преобразование является недопустимым.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307800"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="e0a7a-103">Функция Три_парсе (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="e0a7a-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="e0a7a-104">Выполняет синтаксический анализ текстового значения до указанного типа данных в культуре приложения или возвращает значение null, если преобразование является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0a7a-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="e0a7a-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="e0a7a-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e0a7a-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e0a7a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0a7a-107">Syntax</span></span>

 <span data-ttu-id="e0a7a-108">**Три_парсе** (*Текстекспрессион*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="e0a7a-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="e0a7a-109">Функция **три_парсе** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e0a7a-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="e0a7a-110">**Argument name**</span></span>|<span data-ttu-id="e0a7a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e0a7a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e0a7a-112">*Текстекспрессион*</span><span class="sxs-lookup"><span data-stu-id="e0a7a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="e0a7a-113">Текстовое выражение, представляющее форматированное значение, которое необходимо проанализировать в указанный тип данных.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="e0a7a-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="e0a7a-114">*DataType*</span></span>  <br/> |<span data-ttu-id="e0a7a-115">Тип данных, в который необходимо проанализировать *текстекспрессион* .</span><span class="sxs-lookup"><span data-stu-id="e0a7a-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0a7a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="e0a7a-116">Remarks</span></span>

<span data-ttu-id="e0a7a-117">Используйте **три_парсе** только для преобразования из String в типы даты/времени и Number.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="e0a7a-118">Для преобразования общих типов продолжайте использовать **Convert**.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-118">For general type conversions, continue to use **Convert**.</span></span> 
  

