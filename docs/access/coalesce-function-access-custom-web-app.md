---
title: Функция объединения функции (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Возвращает первое выражение, которое не имеет значение NULL, из списка аргументов.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806955"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="ac9e6-103">Функция объединения функции (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="ac9e6-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="ac9e6-104">Возвращает первое выражение, которое не имеет значение NULL, из списка аргументов.</span><span class="sxs-lookup"><span data-stu-id="ac9e6-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ac9e6-105">Компонент хранилища облаке, описанных в этой статье в Office 2013 и Office 2016 больше не поддерживается и может привести следующее сообщение об ошибке: > *к сожалению, мы возникают проблемы с сервера, поэтому мы не удается добавить \<службы\> на данный момент. Повторите попытку позже.*</span><span class="sxs-lookup"><span data-stu-id="ac9e6-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="ac9e6-106">> Для облачного хранилища для Microsoft Office Online, Office для операций ввода-вывода и Office для Android можно найти в нашем [Партнерской программы Office облачных хранилища](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ac9e6-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ac9e6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac9e6-107">Syntax</span></span>

<span data-ttu-id="ac9e6-108">**Функция объединения** (*Значение*, [*значение*],..., [*значение*])</span><span class="sxs-lookup"><span data-stu-id="ac9e6-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="ac9e6-109">Функция **Объединение** содержит следующие аргументы</span><span class="sxs-lookup"><span data-stu-id="ac9e6-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="ac9e6-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="ac9e6-110">**Argument name**</span></span>|<span data-ttu-id="ac9e6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac9e6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ac9e6-112">*Значение*</span><span class="sxs-lookup"><span data-stu-id="ac9e6-112">*Value*</span></span>  <br/> |<span data-ttu-id="ac9e6-113">Выражение.</span><span class="sxs-lookup"><span data-stu-id="ac9e6-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac9e6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac9e6-114">Remarks</span></span>

<span data-ttu-id="ac9e6-115">Если все аргументы имеют значение NULL, **Объединение** возвращает значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ac9e6-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ac9e6-116">Пример</span><span class="sxs-lookup"><span data-stu-id="ac9e6-116">Example</span></span>

<span data-ttu-id="ac9e6-117">Следующее выражение используется как правила проверки для таблицы.</span><span class="sxs-lookup"><span data-stu-id="ac9e6-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="ac9e6-118">Выражение гарантирует, что записи вносятся в поля имя, последнее имя электронной почты, мобильный телефон, рабочего телефона, домашней телефона, и компаниями перед сохранением записи.</span><span class="sxs-lookup"><span data-stu-id="ac9e6-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="ac9e6-119">Если какие-либо из перечисленных полей незаполненными, функция **объединения** возвращает Null, которые нарушают правило проверки.</span><span class="sxs-lookup"><span data-stu-id="ac9e6-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


