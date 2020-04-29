---
title: Советы по работе с таблицами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439739"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="e3cca-103">Советы по работе с таблицами</span><span class="sxs-lookup"><span data-stu-id="e3cca-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="e3cca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3cca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3cca-105">Работа с таблицей MAPI немного похожа на работу с таблицей реляционной базы данных.</span><span class="sxs-lookup"><span data-stu-id="e3cca-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="e3cca-106">Пользователь может ограничить количество строк и столбцов в представлении и указать их порядок.</span><span class="sxs-lookup"><span data-stu-id="e3cca-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="e3cca-107">Строки можно извлекать по одному или по группам.</span><span class="sxs-lookup"><span data-stu-id="e3cca-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="e3cca-108">Курсор, который отслеживает текущую позицию, можно переместить в определенное место в таблице.</span><span class="sxs-lookup"><span data-stu-id="e3cca-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="e3cca-109">Для работы с таблицами Клиенты используют интерфейс "только для чтения", [IMAPITable: IUnknown](imapitableiunknown.md), а поставщикам служб — в зависимости от того, владеют ли они данными, на которых основана таблица, могут использовать либо **IMAPITable** , либо [итабледата: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e3cca-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="e3cca-110">Операции, определенные в этих интерфейсах, можно классифицировать как операции, которые все пользователи таблиц либо могут вызывать, либо могут вызывать и операции, которые не являются широко используемыми, так как они более сложные.</span><span class="sxs-lookup"><span data-stu-id="e3cca-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="e3cca-111">Некоторые расширенные операции более сложны для реализации; другие не сложны, но представляют интерес к небольшому доли компонентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="e3cca-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="e3cca-112">Наиболее распространенные операции:</span><span class="sxs-lookup"><span data-stu-id="e3cca-112">The more common operations are:</span></span>
  
- <span data-ttu-id="e3cca-113">Операции со столбцами, которые применяются к отдельным столбцам.</span><span class="sxs-lookup"><span data-stu-id="e3cca-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="e3cca-114">Сюда входят указания свойств, которые необходимо включить в набор столбцов, и порядок их включения.</span><span class="sxs-lookup"><span data-stu-id="e3cca-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="e3cca-115">Операции со строками, которые влияют на отдельные строки.</span><span class="sxs-lookup"><span data-stu-id="e3cca-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="e3cca-116">К ним относятся извлечение данных и операции обслуживания: Добавление, удаление и изменение одной строки или строк.</span><span class="sxs-lookup"><span data-stu-id="e3cca-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="e3cca-117">Глобальные операции, которые влияют на всю таблицу.</span><span class="sxs-lookup"><span data-stu-id="e3cca-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="e3cca-118">Сюда входят уведомления о событиях, Поиск и сортировка.</span><span class="sxs-lookup"><span data-stu-id="e3cca-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3cca-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e3cca-119">See also</span></span>



[<span data-ttu-id="e3cca-120">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="e3cca-120">MAPI Tables</span></span>](mapi-tables.md)

