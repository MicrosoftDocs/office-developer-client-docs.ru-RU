---
title: Группировка и ограничения таблиц в поставщиках хранилищ сообщений
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
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="cf41e-103">Группировка и ограничения таблиц в поставщиках хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="cf41e-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="cf41e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf41e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf41e-105">Клиентские приложения часто позволяют пользователям управлять способом отображения содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="cf41e-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="cf41e-106">Как правило, пользователи могут группировать сообщения в соответствии со значением одного или нескольких свойств сообщения или могут исключать сообщения, соответствующие определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="cf41e-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="cf41e-107">Это делается с помощью интерфейса [IMAPITable: IUnknown](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="cf41e-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="cf41e-108">Клиентские приложения могут запрещать строкам, возвращаемым из таблицы, любые критерии, заданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="cf41e-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="cf41e-109">Поэтому поставщику хранилища сообщений необходимо реализовать следующие методы **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="cf41e-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="cf41e-110">Метод IMAPITable \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cf41e-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="cf41e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cf41e-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf41e-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="cf41e-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="cf41e-113">Возвращает строки таблицы, которые отвечают заданным условиям.</span><span class="sxs-lookup"><span data-stu-id="cf41e-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="cf41e-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="cf41e-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="cf41e-115">Возвращает набор столбцов в таблице или набор столбцов, используемых в текущий момент.</span><span class="sxs-lookup"><span data-stu-id="cf41e-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="cf41e-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="cf41e-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="cf41e-117">Возвращает одну или несколько строк из таблицы, начиная с заданной позиции.</span><span class="sxs-lookup"><span data-stu-id="cf41e-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="cf41e-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="cf41e-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="cf41e-119">ПриМеняет ограничение к таблице, чтобы последующие вызовы метода **FindRow** возвращали только строки, соответствующие ограничению.</span><span class="sxs-lookup"><span data-stu-id="cf41e-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="cf41e-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="cf41e-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="cf41e-121">Указывает, какие столбцы должны возвращаться при извлечении строк из таблицы.</span><span class="sxs-lookup"><span data-stu-id="cf41e-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="cf41e-122">Ограничения могут быть сложными для реализации; более подробную информацию можно узнать в статье [ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="cf41e-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="cf41e-123">Дополнительные сведения о реализации таблиц содержатся в статье [MAPI Tables](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cf41e-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf41e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="cf41e-124">See also</span></span>



[<span data-ttu-id="cf41e-125">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="cf41e-125">Message Store Features</span></span>](message-store-features.md)

