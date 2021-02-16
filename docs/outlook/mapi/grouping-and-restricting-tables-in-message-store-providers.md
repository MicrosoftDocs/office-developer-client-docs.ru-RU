---
title: Группировка и ограничение таблиц в поставщиках store сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428986"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="c7d65-103">Группировка и ограничение таблиц в поставщиках store сообщений</span><span class="sxs-lookup"><span data-stu-id="c7d65-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="c7d65-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7d65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7d65-105">Клиентские приложения часто позволяют пользователям контролировать отображение содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="c7d65-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="c7d65-106">Как правило, пользователь может выбрать группу сообщений в соответствии со значением одного или более свойств сообщения или исключить сообщения, которые соответствуют определенным критериям.</span><span class="sxs-lookup"><span data-stu-id="c7d65-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="c7d65-107">Для этого используется интерфейс [IMAPITable : IUnknown.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="c7d65-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="c7d65-108">Клиентские приложения могут ограничить строки, возвращенные из таблицы, любыми критериями, заданными пользователем.</span><span class="sxs-lookup"><span data-stu-id="c7d65-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="c7d65-109">Поэтому поставщику store сообщений необходимо реализовать следующие методы **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="c7d65-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="c7d65-110">Метод IMAPITable\*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="c7d65-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="c7d65-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7d65-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7d65-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="c7d65-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="c7d65-113">Возвращает строки таблиц, которые соответствуют заданным условиям.</span><span class="sxs-lookup"><span data-stu-id="c7d65-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="c7d65-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c7d65-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="c7d65-115">Возвращает набор столбцов в таблице или набор используемых в настоящее время столбцов.</span><span class="sxs-lookup"><span data-stu-id="c7d65-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="c7d65-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c7d65-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="c7d65-117">Возвращает одну или несколько строк из таблицы, начиная с заданной позиции.</span><span class="sxs-lookup"><span data-stu-id="c7d65-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="c7d65-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="c7d65-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="c7d65-119">Применяет ограничение к таблице, чтобы последующие вызовы **FindRow** возвращали только строки, которые соответствуют ограничению.</span><span class="sxs-lookup"><span data-stu-id="c7d65-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="c7d65-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c7d65-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="c7d65-121">Указывает, какие столбцы должны возвращаться при извлечении строк из таблицы.</span><span class="sxs-lookup"><span data-stu-id="c7d65-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="c7d65-122">Реализация ограничений может быть сложной; дополнительные сведения [см. в сведениях об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="c7d65-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="c7d65-123">Дополнительные сведения о реализации таблиц см. в [таблицах MAPI.](mapi-tables.md)</span><span class="sxs-lookup"><span data-stu-id="c7d65-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7d65-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c7d65-124">See also</span></span>



[<span data-ttu-id="c7d65-125">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="c7d65-125">Message Store Features</span></span>](message-store-features.md)

