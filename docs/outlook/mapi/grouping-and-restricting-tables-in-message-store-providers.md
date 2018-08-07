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
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808549"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="20440-103">Группировка и ограничение таблиц в поставщиках хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="20440-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="20440-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20440-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20440-105">Клиентские приложения часто позволяют пользователям управлять способ отображения содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="20440-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="20440-106">Как правило пользователь можно выбрать для сообщений, сгруппированных по значение одного или нескольких свойств сообщения или исключить сообщения, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="20440-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="20440-107">Это делается с помощью [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="20440-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="20440-108">Клиентские приложения можно ограничить строк, возвращенных из таблицы для любой пользователь вводит условия.</span><span class="sxs-lookup"><span data-stu-id="20440-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="20440-109">Таким образом сообщение хранилища поставщика необходимо реализовать следующие методы **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="20440-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="20440-110">IMAPITable ** метод **</span><span class="sxs-lookup"><span data-stu-id="20440-110">****IMAPITable** method**</span></span>|<span data-ttu-id="20440-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20440-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20440-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="20440-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="20440-113">Возвращает таблицы строк, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="20440-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="20440-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="20440-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="20440-115">Возвращает набор столбцов в таблице или наборы столбцов, используемых в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="20440-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="20440-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="20440-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="20440-117">Возвращает один или несколько строк из таблицы, начиная с заданной позиции.</span><span class="sxs-lookup"><span data-stu-id="20440-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="20440-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="20440-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="20440-119">Применяет ограничение в таблицу, чтобы последующие вызовы **FindRow** возвращать только строки, соответствующие ограничение.</span><span class="sxs-lookup"><span data-stu-id="20440-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="20440-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="20440-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="20440-121">Указывает, какие столбцы должны возвращаться при строки извлекаются из таблицы.</span><span class="sxs-lookup"><span data-stu-id="20440-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="20440-122">Ограничения может быть сложной для реализации; Для получения дополнительных сведений обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="20440-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="20440-123">Дополнительные сведения о реализации таблицы [MAPI](mapi-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="20440-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20440-124">См. также</span><span class="sxs-lookup"><span data-stu-id="20440-124">See also</span></span>



[<span data-ttu-id="20440-125">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="20440-125">Message Store Features</span></span>](message-store-features.md)

