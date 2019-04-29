---
title: Функция объединения (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Возвращает первое выражение, не равное NULL, из списка аргументов.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411395"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="50476-103">Функция объединения (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="50476-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="50476-104">Возвращает первое выражение, не равное NULL, из списка аргументов.</span><span class="sxs-lookup"><span data-stu-id="50476-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="50476-105">Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="50476-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="50476-106">Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="50476-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="50476-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50476-107">Syntax</span></span>

<span data-ttu-id="50476-108">**Объединение** (*Значение*, [*значение*],..., [*значение*])</span><span class="sxs-lookup"><span data-stu-id="50476-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="50476-109">Функция **объединения** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="50476-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="50476-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="50476-110">**Argument name**</span></span>|<span data-ttu-id="50476-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="50476-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="50476-112">*Значение*</span><span class="sxs-lookup"><span data-stu-id="50476-112">*Value*</span></span>  <br/> |<span data-ttu-id="50476-113">Выражение.</span><span class="sxs-lookup"><span data-stu-id="50476-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50476-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="50476-114">Remarks</span></span>

<span data-ttu-id="50476-115">Если все аргументы имеют значение NULL, функция **объединения** ВОЗВРАЩАЕТ значение null.</span><span class="sxs-lookup"><span data-stu-id="50476-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="50476-116">Пример</span><span class="sxs-lookup"><span data-stu-id="50476-116">Example</span></span>

<span data-ttu-id="50476-117">В качестве правила проверки для таблицы используется следующее выражение.</span><span class="sxs-lookup"><span data-stu-id="50476-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="50476-118">Выражение гарантирует, что записи будут введены в виде имени, фамилии, электронной почты, мобильного телефона, рабочего телефона, домашнего телефона и поля компании перед фиксацией записи.</span><span class="sxs-lookup"><span data-stu-id="50476-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="50476-119">Если любое из указанных полей остается пустым, функция **объединения** возвращает значение null, что нарушает правило проверки.</span><span class="sxs-lookup"><span data-stu-id="50476-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


