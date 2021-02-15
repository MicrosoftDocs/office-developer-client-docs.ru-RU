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
# <a name="chapter-6-error-handling"></a><span data-ttu-id="0cb51-102">Глава 6. Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="0cb51-102">Chapter 6: Error handling</span></span>

<span data-ttu-id="0cb51-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cb51-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0cb51-104">ADO использует несколько различных методов для уведомления приложения о возникая ошибках.</span><span class="sxs-lookup"><span data-stu-id="0cb51-104">ADO uses several different methods to notify an application of errors that occur.</span></span> <span data-ttu-id="0cb51-105">В этой главе обсуждаются типы ошибок, которые могут возникать при использовании ADO, и то, как приложение уведомлено.</span><span class="sxs-lookup"><span data-stu-id="0cb51-105">This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified.</span></span> <span data-ttu-id="0cb51-106">В завершение в окну вы можете в принятия решений об обработке этих ошибок.</span><span class="sxs-lookup"><span data-stu-id="0cb51-106">It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="0cb51-107">How does ADO report errors?</span><span class="sxs-lookup"><span data-stu-id="0cb51-107">How does ADO report errors?</span></span>

<span data-ttu-id="0cb51-108">ADO сообщает об ошибках несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="0cb51-108">ADO notifies you about errors in several ways:</span></span>

- <span data-ttu-id="0cb51-109">Ошибки ADO создают ошибку времени запуска.</span><span class="sxs-lookup"><span data-stu-id="0cb51-109">ADO errors generate a run-time error.</span></span> <span data-ttu-id="0cb51-110">Обработать ошибку ADO так же, как и любую другую  ошибку во время Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0cb51-110">Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

- <span data-ttu-id="0cb51-111">Программа может получать ошибки из OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0cb51-111">Your program can receive errors from OLE DB.</span></span> <span data-ttu-id="0cb51-112">Ошибка OLE DB также создает ошибку времени запуска.</span><span class="sxs-lookup"><span data-stu-id="0cb51-112">An OLE DB error generates a run-time error as well.</span></span>

- <span data-ttu-id="0cb51-113">Если ошибка характерна для поставщика данных, один или несколько объектов **Error** помещаются в коллекцию **errors** объекта **Connection,** который использовался для доступа к хранию данных во время ошибки.</span><span class="sxs-lookup"><span data-stu-id="0cb51-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

- <span data-ttu-id="0cb51-114">Если процесс, который вызывает событие, также вызывает ошибку, сведения об ошибке помещаются в объект **Error** и передаются в качестве параметра событию.</span><span class="sxs-lookup"><span data-stu-id="0cb51-114">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event.</span></span> <span data-ttu-id="0cb51-115">Дополнительные сведения о событиях см. в главе [7 "Обработка](chapter-7-handling-ado-events.md) событий ADO".</span><span class="sxs-lookup"><span data-stu-id="0cb51-115">See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

- <span data-ttu-id="0cb51-116">Проблемы, которые возникают при обработке пакетных обновлений или других массовых операций, связанных с набором **записей,** могут быть указаны свойством **Status** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="0cb51-116">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**.</span></span> <span data-ttu-id="0cb51-117">Например, в значениях **RecordStatusEnum** могут быть указаны нарушения ограничения схемы или недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="0cb51-117">For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

- <span data-ttu-id="0cb51-118">Проблемы, связанные с  определенным полем в текущей записи, также  указываются свойством **Status** каждого поля в коллекции **Fields** объекта **Record** или **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="0cb51-118">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**.</span></span> <span data-ttu-id="0cb51-119">Например, обновления, которые не удалось завершить или несовместимые типы данных, могут быть заданы **значениями FieldStatusEnum.**</span><span class="sxs-lookup"><span data-stu-id="0cb51-119">For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="0cb51-120">В следующих разделах каждый из этих методов уведомлений описан более подробно.</span><span class="sxs-lookup"><span data-stu-id="0cb51-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="0cb51-121">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="0cb51-121">ADO errors</span></span>](ado-errors.md)
- [<span data-ttu-id="0cb51-122">Справочник по ошибкам ADO</span><span class="sxs-lookup"><span data-stu-id="0cb51-122">ADO error reference</span></span>](ado-error-reference.md)
- [<span data-ttu-id="0cb51-123">Ошибки поставщиков</span><span class="sxs-lookup"><span data-stu-id="0cb51-123">Provider errors</span></span>](provider-errors.md)
- [<span data-ttu-id="0cb51-124">Сведения об ошибках, связанных с полями</span><span class="sxs-lookup"><span data-stu-id="0cb51-124">Field-related error information</span></span>](field-related-error-information.md)
- [<span data-ttu-id="0cb51-125">Сведения об ошибках, связанных с наборами записей</span><span class="sxs-lookup"><span data-stu-id="0cb51-125">Recordset-related error information</span></span>](recordset-related-error-information.md)
- [<span data-ttu-id="0cb51-126">Предугадывание ошибок</span><span class="sxs-lookup"><span data-stu-id="0cb51-126">Anticipating errors</span></span>](anticipating-errors.md)
- [<span data-ttu-id="0cb51-127">Обработка ошибок на других языках (ADO)</span><span class="sxs-lookup"><span data-stu-id="0cb51-127">Handling errors in other languages (ADO)</span></span>](handling-errors-in-other-languages.md)
