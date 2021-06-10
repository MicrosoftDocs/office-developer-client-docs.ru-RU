---
title: Глава 6. Обработка ошибок
TOCTitle: 'Chapter 6: Error handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14d3dc4b291d96a47e0fb67c0e7d837463cd4bf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296411"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="c8030-102">Глава 6. Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="c8030-102">Chapter 6: Error handling</span></span>

<span data-ttu-id="c8030-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8030-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8030-104">ADO использует несколько различных методов, чтобы уведомить приложение об ошибках, которые происходят.</span><span class="sxs-lookup"><span data-stu-id="c8030-104">ADO uses several different methods to notify an application of errors that occur.</span></span> <span data-ttu-id="c8030-105">В этой главе обсуждаются типы ошибок, которые могут возникать при использовании ADO, и то, как ваше приложение уведомлено.</span><span class="sxs-lookup"><span data-stu-id="c8030-105">This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified.</span></span> <span data-ttu-id="c8030-106">В заключение он внося предложения по обработке этих ошибок.</span><span class="sxs-lookup"><span data-stu-id="c8030-106">It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="c8030-107">How does ADO report errors?</span><span class="sxs-lookup"><span data-stu-id="c8030-107">How does ADO report errors?</span></span>

<span data-ttu-id="c8030-108">ADO сообщает вам об ошибках несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="c8030-108">ADO notifies you about errors in several ways:</span></span>

- <span data-ttu-id="c8030-109">Ошибки ADO создают ошибку во время запуска.</span><span class="sxs-lookup"><span data-stu-id="c8030-109">ADO errors generate a run-time error.</span></span> <span data-ttu-id="c8030-110">Справься с ошибкой ADO так же, как и  с любой другой ошибкой во время запуска, например с помощью заявления об ошибке в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c8030-110">Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

- <span data-ttu-id="c8030-111">Ваша программа может получать ошибки из OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c8030-111">Your program can receive errors from OLE DB.</span></span> <span data-ttu-id="c8030-112">Ошибка OLE DB также создает ошибку времени запуска.</span><span class="sxs-lookup"><span data-stu-id="c8030-112">An OLE DB error generates a run-time error as well.</span></span>

- <span data-ttu-id="c8030-113">Если ошибка имеет отношение к поставщику  данных, один или  несколько объектов ошибки помещаются в коллекцию Ошибок объекта **Connection,** который использовался для доступа к хранилище данных при ошибке.</span><span class="sxs-lookup"><span data-stu-id="c8030-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

- <span data-ttu-id="c8030-114">Если в процессе, в результате который было поднято событие, также произошла ошибка, сведения об ошибке помещаются в объект **Error** и передаются в качестве параметра для события.</span><span class="sxs-lookup"><span data-stu-id="c8030-114">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event.</span></span> <span data-ttu-id="c8030-115">Дополнительные сведения о событиях см. в главе [7. Обработка событий ADO.](chapter-7-handling-ado-events.md)</span><span class="sxs-lookup"><span data-stu-id="c8030-115">See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

- <span data-ttu-id="c8030-116">Проблемы, которые возникают при обработке пакетных обновлений или других массовых операций, связанных с **набором** записей, могут быть указаны **свойством Status** of the **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c8030-116">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**.</span></span> <span data-ttu-id="c8030-117">Например, нарушения ограничения схемы или недостаточные разрешения могут быть указаны **значениями RecordStatusEnum.**</span><span class="sxs-lookup"><span data-stu-id="c8030-117">For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

- <span data-ttu-id="c8030-118">Проблемы, которые возникают  с участием определенного поля в текущей записи, также указываются свойством **Status** каждого поля в коллекции **Полей** **record** или **Recordset.** </span><span class="sxs-lookup"><span data-stu-id="c8030-118">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**.</span></span> <span data-ttu-id="c8030-119">Например, обновления, которые не удалось завершить или несовместимые типы данных, могут быть указаны **значениями FieldStatusEnum.**</span><span class="sxs-lookup"><span data-stu-id="c8030-119">For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="c8030-120">В следующих разделах описаны все эти методы уведомления более подробно.</span><span class="sxs-lookup"><span data-stu-id="c8030-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="c8030-121">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="c8030-121">ADO errors</span></span>](ado-errors.md)
- [<span data-ttu-id="c8030-122">Справочник по ошибкам ADO</span><span class="sxs-lookup"><span data-stu-id="c8030-122">ADO error reference</span></span>](ado-error-reference.md)
- [<span data-ttu-id="c8030-123">Ошибки поставщиков</span><span class="sxs-lookup"><span data-stu-id="c8030-123">Provider errors</span></span>](provider-errors.md)
- [<span data-ttu-id="c8030-124">Сведения об ошибках, связанных с полями</span><span class="sxs-lookup"><span data-stu-id="c8030-124">Field-related error information</span></span>](field-related-error-information.md)
- [<span data-ttu-id="c8030-125">Сведения об ошибках, связанных с наборами записей</span><span class="sxs-lookup"><span data-stu-id="c8030-125">Recordset-related error information</span></span>](recordset-related-error-information.md)
- [<span data-ttu-id="c8030-126">Предугадывание ошибок</span><span class="sxs-lookup"><span data-stu-id="c8030-126">Anticipating errors</span></span>](anticipating-errors.md)
- [<span data-ttu-id="c8030-127">Обработка ошибок на других языках (ADO)</span><span class="sxs-lookup"><span data-stu-id="c8030-127">Handling errors in other languages (ADO)</span></span>](handling-errors-in-other-languages.md)
