---
title: Свойство Recordset2.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309105"
---
# <a name="recordset2updateoptions-property-dao"></a><span data-ttu-id="490d6-102">Свойство Recordset2.UpdateOptions (DAO)</span><span class="sxs-lookup"><span data-stu-id="490d6-102">Recordset2.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="490d6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="490d6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="490d6-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="490d6-104">Syntax</span></span>

<span data-ttu-id="490d6-105">*выражения* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="490d6-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="490d6-106">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="490d6-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="490d6-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="490d6-107">Remarks</span></span>

<span data-ttu-id="490d6-108">При выполнении **[](recordset2-update-method-dao.md)** обновления пакетного режима DAO и клиентская библиотека курсоров пакетных пакетов создают ряд SQL update для внесения необходимых изменений.</span><span class="sxs-lookup"><span data-stu-id="490d6-108">When a batch-mode **[Update](recordset2-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="490d6-109">Для SQL, чтобы изолировать записи, которые помечены как измененные **[свойством RecordStatus,](recordset2-recordstatus-property-dao.md)** создается пункт where.</span><span class="sxs-lookup"><span data-stu-id="490d6-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset2-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="490d6-110">Так как на некоторых удаленных серверах используются триггеры или другие способы обеспечения целостности ссылок, часто важно ограничить поля, обновляемые только теми, которые затронуты изменением.</span><span class="sxs-lookup"><span data-stu-id="490d6-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="490d6-111">Для этого установите свойство **UpdateOptions** в одну из констант **dbCriteriaKey,** **dbCriteriaModValues,** **dbCriteriaAllCols** или **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="490d6-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="490d6-112">Таким образом выполняется только абсолютное минимальное количество триггерного кода.</span><span class="sxs-lookup"><span data-stu-id="490d6-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="490d6-113">В результате операция обновления выполняется быстрее и имеет меньше потенциальных ошибок.</span><span class="sxs-lookup"><span data-stu-id="490d6-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="490d6-114">Вы также можете умиротворять константы **dbCriteriaDeleteInsert** или **dbCriteriaUpdate,** чтобы определить, следует ли использовать набор заявлений SQL DELETE и INSERT или SQL UPDATE для каждого обновления при отправке пакетных изменений обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="490d6-114">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server.</span></span> <span data-ttu-id="490d6-115">В этом случае для обновления записи требуется две отдельные операции.</span><span class="sxs-lookup"><span data-stu-id="490d6-115">In the former case, two separate operations are required to update the record.</span></span> <span data-ttu-id="490d6-116">В некоторых случаях, особенно если удаленная система реализует триггеры DELETE, INSERT и UPDATE, выбор правильного параметра **свойства UpdateOptions** может существенно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="490d6-116">In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="490d6-117">Если не указать константы, будут использоваться **dbCriteriaUpdate** и **dbCriteriaKey.**</span><span class="sxs-lookup"><span data-stu-id="490d6-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="490d6-118">Добавленные записи всегда будут создавать заявления INSERT, а удаленные записи всегда будут создавать заявления DELETE, поэтому это свойство применимо только к обновлению модифицированных записей библиотеки курсоров.</span><span class="sxs-lookup"><span data-stu-id="490d6-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

