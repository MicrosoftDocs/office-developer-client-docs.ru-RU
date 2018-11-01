---
title: Глава 6. Обработка ошибок
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec3a8972f8ca46754971eee7e8aa4a70c367a349
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868331"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="e0d51-102">Глава 6. Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="e0d51-102">Chapter 6: Error Handling</span></span>


<span data-ttu-id="e0d51-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0d51-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0d51-104">ADO использует несколько различных методов для уведомлять приложение возникающие ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0d51-104">ADO uses several different methods to notify an application of errors that occur.</span></span> <span data-ttu-id="e0d51-105">В этой главе рассматриваются типы ошибок, которые могут возникнуть при использовании ADO и способ уведомления приложения.</span><span class="sxs-lookup"><span data-stu-id="e0d51-105">This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified.</span></span> <span data-ttu-id="e0d51-106">Он завершается внесения предложения о том, как обрабатывать эти ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0d51-106">It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="e0d51-107">Как ADO отчет ошибки</span><span class="sxs-lookup"><span data-stu-id="e0d51-107">How Does ADO Report Errors?</span></span>

<span data-ttu-id="e0d51-108">ADO уведомления об ошибках несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="e0d51-108">ADO notifies you about errors in several ways:</span></span>

  - <span data-ttu-id="e0d51-109">Ошибки ADO вызывают ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e0d51-109">ADO errors generate a run-time error.</span></span> <span data-ttu-id="e0d51-110">Обрабатывать ошибки ADO так же, как любая другая ошибка времени выполнения, например, с помощью оператора **On Error** в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e0d51-110">Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

  - <span data-ttu-id="e0d51-111">Программы могут получать ошибки OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e0d51-111">Your program can receive errors from OLE DB.</span></span> <span data-ttu-id="e0d51-112">Ошибка OLE DB генерирует ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e0d51-112">An OLE DB error generates a run-time error as well.</span></span>

  - <span data-ttu-id="e0d51-113">Если ошибка является специально для поставщика данных, один или несколько объектов **Ошибка** помещаются в семействе **Errors** объекта **подключения** , который использовался для доступа к хранилищу данных при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0d51-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

  - <span data-ttu-id="e0d51-114">Если процесс, который вызвал событие, также создаваемый ошибку, сведения об ошибке помещаются в объект **Error** и передается как параметр событию.</span><span class="sxs-lookup"><span data-stu-id="e0d51-114">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event.</span></span> <span data-ttu-id="e0d51-115">Просмотреть [Глава 7: обработка событий ADO](chapter-7-handling-ado-events.md) Дополнительные сведения о событиях.</span><span class="sxs-lookup"><span data-stu-id="e0d51-115">See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

  - <span data-ttu-id="e0d51-116">Проблемы, возникающие при обработке пакета обновлений или других массовые операции, включающие использование **записей** может быть указан в свойстве **состояние** **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e0d51-116">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**.</span></span> <span data-ttu-id="e0d51-117">Например нарушения ограничения схемы или разрешений можно задать с **RecordStatusEnum** значения.</span><span class="sxs-lookup"><span data-stu-id="e0d51-117">For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

  - <span data-ttu-id="e0d51-118">Проблемы, возникающие, включающие использование отдельного **поля** в текущей записи также указываются свойство **Status** каждое **поле** в коллекции **полей** **записи** или **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e0d51-118">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**.</span></span> <span data-ttu-id="e0d51-119">Например обновлений, которые не удалось завершить или типы несовместимые данные можно задать с **FieldStatusEnum** значения.</span><span class="sxs-lookup"><span data-stu-id="e0d51-119">For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="e0d51-120">В следующих разделах каждый из этих методов уведомлений более подробно.</span><span class="sxs-lookup"><span data-stu-id="e0d51-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="e0d51-121">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="e0d51-121">ADO Errors</span></span>](ado-errors.md)

- [<span data-ttu-id="e0d51-122">Справочник по об ошибках ADO</span><span class="sxs-lookup"><span data-stu-id="e0d51-122">ADO Error Reference</span></span>](ado-error-reference.md)

- [<span data-ttu-id="e0d51-123">Ошибки поставщиков</span><span class="sxs-lookup"><span data-stu-id="e0d51-123">Provider Errors</span></span>](provider-errors.md)

- [<span data-ttu-id="e0d51-124">Сведения об ошибках, связанных с полями</span><span class="sxs-lookup"><span data-stu-id="e0d51-124">Field-Related Error Information</span></span>](field-related-error-information.md)

- [<span data-ttu-id="e0d51-125">Сведения об ошибках, связанных с наборами записей</span><span class="sxs-lookup"><span data-stu-id="e0d51-125">Recordset-Related Error Information</span></span>](recordset-related-error-information.md)

- [<span data-ttu-id="e0d51-126">Предугадывание ошибок</span><span class="sxs-lookup"><span data-stu-id="e0d51-126">Anticipating Errors</span></span>](anticipating-errors.md)

- [<span data-ttu-id="e0d51-127">Handling Errors in Other Languages (ADO)</span><span class="sxs-lookup"><span data-stu-id="e0d51-127">Handling Errors in Other Languages (ADO)</span></span>](handling-errors-in-other-languages.md)