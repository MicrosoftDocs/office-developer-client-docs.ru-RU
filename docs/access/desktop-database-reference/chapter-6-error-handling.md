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
# <a name="chapter-6-error-handling"></a><span data-ttu-id="7c9c4-102">Глава 6. Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="7c9c4-102">Chapter 6: Error handling</span></span>

<span data-ttu-id="7c9c4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c9c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c9c4-104">ADO использует несколько различных способов уведомления о возможном возникновении ошибок.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-104">ADO uses several different methods to notify an application of errors that occur.</span></span> <span data-ttu-id="7c9c4-105">В этой главе обсуждаются типы ошибок, которые могут возникать при использовании ADO и способ уведомления приложения.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-105">This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified.</span></span> <span data-ttu-id="7c9c4-106">Она завершается путем предоставления предложений об обработке этих ошибок.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-106">It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="7c9c4-107">Как ADO сообщать об ошибках?</span><span class="sxs-lookup"><span data-stu-id="7c9c4-107">How does ADO report errors?</span></span>

<span data-ttu-id="7c9c4-108">ADO уведомляет об ошибках несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="7c9c4-108">ADO notifies you about errors in several ways:</span></span>

- <span data-ttu-id="7c9c4-109">Ошибки во время выполнения генерируют ошибки ADO.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-109">ADO errors generate a run-time error.</span></span> <span data-ttu-id="7c9c4-110">Обработка ошибки ADO аналогично любой другой ошибке во время выполнения, например, при использовании оператора **On Error** в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-110">Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

- <span data-ttu-id="7c9c4-111">Программа может получать ошибки из OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-111">Your program can receive errors from OLE DB.</span></span> <span data-ttu-id="7c9c4-112">Ошибка во время выполнения также возникает при возникновении ошибки OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-112">An OLE DB error generates a run-time error as well.</span></span>

- <span data-ttu-id="7c9c4-113">Если ошибка относится к поставщику данных, в коллекцию Errors объекта **Connection** , который использовался для \*\*\*\* доступа к хранилищу данных при возникновении ошибки, помещается один или несколько объектов **Error** .</span><span class="sxs-lookup"><span data-stu-id="7c9c4-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

- <span data-ttu-id="7c9c4-114">Если процесс, вызвавший событие, также вызвал ошибку, сведения об ошибке помещается в объект **Error** и передаются в качестве параметра для события.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-114">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event.</span></span> <span data-ttu-id="7c9c4-115">Дополнительные сведения о событиях можно найти в [главе 7: обработка событий ADO](chapter-7-handling-ado-events.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9c4-115">See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

- <span data-ttu-id="7c9c4-116">Проблемы, возникающие при обработке пакетных обновлений или других массовых операций с использованием объекта **Recordset** , могут быть указаны в свойстве **Status** объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-116">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**.</span></span> <span data-ttu-id="7c9c4-117">Например, значения **RecordStatusEnum** могут задаваться нарушениями ограничений схемы или недостаточными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-117">For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

- <span data-ttu-id="7c9c4-118">Проблемы, возникающие при возникновении определенного **поля** в текущей записи, также указываются в свойстве **Status** каждого **поля** в коллекции **Fields** **записи** или **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-118">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**.</span></span> <span data-ttu-id="7c9c4-119">Например, значения **фиелдстатусенум** могут указывать на обновления, которые не удалось выполнить или с несовместимыми типами данных.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-119">For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="7c9c4-120">В следующих разделах подробно описывается каждый из этих методов уведомления.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="7c9c4-121">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="7c9c4-121">ADO errors</span></span>](ado-errors.md)
- [<span data-ttu-id="7c9c4-122">Справочник по ошибкам ADO</span><span class="sxs-lookup"><span data-stu-id="7c9c4-122">ADO error reference</span></span>](ado-error-reference.md)
- [<span data-ttu-id="7c9c4-123">Ошибки поставщиков</span><span class="sxs-lookup"><span data-stu-id="7c9c4-123">Provider errors</span></span>](provider-errors.md)
- [<span data-ttu-id="7c9c4-124">Сведения об ошибках, связанных с полями</span><span class="sxs-lookup"><span data-stu-id="7c9c4-124">Field-related error information</span></span>](field-related-error-information.md)
- [<span data-ttu-id="7c9c4-125">Сведения об ошибках, связанных с наборами записей</span><span class="sxs-lookup"><span data-stu-id="7c9c4-125">Recordset-related error information</span></span>](recordset-related-error-information.md)
- [<span data-ttu-id="7c9c4-126">Предугадывание ошибок</span><span class="sxs-lookup"><span data-stu-id="7c9c4-126">Anticipating errors</span></span>](anticipating-errors.md)
- [<span data-ttu-id="7c9c4-127">Обработка ошибок на других языках (ADO)</span><span class="sxs-lookup"><span data-stu-id="7c9c4-127">Handling errors in other languages (ADO)</span></span>](handling-errors-in-other-languages.md)
