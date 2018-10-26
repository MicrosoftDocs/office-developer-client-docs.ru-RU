---
title: Группировка и ограничение таблиц в поставщиках хранилищ сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec1c07a8d2c88680ebd94cf8ecd6901ed86ad100
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578789"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="40dc5-103">Группировка и ограничение таблиц в поставщиках хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="40dc5-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="40dc5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40dc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40dc5-105">Клиентские приложения часто позволяют пользователям управлять способ отображения содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="40dc5-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="40dc5-106">Как правило пользователь можно выбрать для сообщений, сгруппированных по значение одного или нескольких свойств сообщения или исключить сообщения, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="40dc5-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="40dc5-107">Это делается с помощью [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="40dc5-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="40dc5-108">Клиентские приложения можно ограничить строк, возвращенных из таблицы для любой пользователь вводит условия.</span><span class="sxs-lookup"><span data-stu-id="40dc5-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="40dc5-109">Таким образом сообщение хранилища поставщика необходимо реализовать следующие методы **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="40dc5-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="40dc5-110">IMAPITable \*\* метод \*\*</span><span class="sxs-lookup"><span data-stu-id="40dc5-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="40dc5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="40dc5-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40dc5-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="40dc5-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="40dc5-113">Возвращает таблицы строк, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="40dc5-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="40dc5-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="40dc5-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="40dc5-115">Возвращает набор столбцов в таблице или наборы столбцов, используемых в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="40dc5-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="40dc5-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="40dc5-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="40dc5-117">Возвращает один или несколько строк из таблицы, начиная с заданной позиции.</span><span class="sxs-lookup"><span data-stu-id="40dc5-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="40dc5-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="40dc5-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="40dc5-119">Применяет ограничение в таблицу, чтобы последующие вызовы **FindRow** возвращать только строки, соответствующие ограничение.</span><span class="sxs-lookup"><span data-stu-id="40dc5-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="40dc5-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="40dc5-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="40dc5-121">Указывает, какие столбцы должны возвращаться при строки извлекаются из таблицы.</span><span class="sxs-lookup"><span data-stu-id="40dc5-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="40dc5-122">Ограничения может быть сложной для реализации; Для получения дополнительных сведений обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="40dc5-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="40dc5-123">Дополнительные сведения о реализации таблицы [MAPI](mapi-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="40dc5-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40dc5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="40dc5-124">See also</span></span>



[<span data-ttu-id="40dc5-125">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="40dc5-125">Message Store Features</span></span>](message-store-features.md)

