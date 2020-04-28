---
title: Свойство Recordset2. UpdateOptions (DAO)
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
# <a name="recordset2updateoptions-property-dao"></a><span data-ttu-id="3f2bd-102">Свойство Recordset2. UpdateOptions (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f2bd-102">Recordset2.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="3f2bd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f2bd-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2bd-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f2bd-104">Syntax</span></span>

<span data-ttu-id="3f2bd-105">*Expression* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="3f2bd-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="3f2bd-106">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3f2bd-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2bd-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f2bd-107">Remarks</span></span>

<span data-ttu-id="3f2bd-108">При выполнении **[обновления](recordset2-update-method-dao.md)** пакетного режима, DAO и библиотека курсора клиентских пакетов создайте ряд инструкций SQL UPDATE, чтобы внести необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-108">When a batch-mode **[Update](recordset2-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="3f2bd-109">Предложение WHERE (SQL) создается для каждого обновления, чтобы изолировать записи, помеченные как измененные свойством **[рекордстатус](recordset2-recordstatus-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="3f2bd-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset2-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="3f2bd-110">Так как некоторые удаленные серверы используют триггеры или другие способы обеспечения целостности данных, часто важно ограничить обновление полей только теми, которые затрагиваются этим изменением.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="3f2bd-111">Для этого присвойте свойству **UpdateOptions** одно из констант **дбкритериакэй**, **дбкритериамодвалуес**, **дбкритериааллколс**или **дбкритериатиместамп**.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="3f2bd-112">Таким образом выполняется только абсолютный минимальный объем кода триггера.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="3f2bd-113">В результате операция обновления выполняется быстрее, и в ней уменьшается количество потенциальных ошибок.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="3f2bd-114">Вы также можете сцепить любую константу **дбкритериаделетеинсерт** или **дбкритериаупдате** , чтобы определить, следует ли использовать набор инструкций SQL DELETE и INSERT или инструкцию SQL UPDATE для каждого обновления при отправке пакетных изменений обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-114">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server.</span></span> <span data-ttu-id="3f2bd-115">В первом случае для обновления записи требуется две отдельные операции.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-115">In the former case, two separate operations are required to update the record.</span></span> <span data-ttu-id="3f2bd-116">В некоторых случаях, особенно когда удаленная система реализует триггеры DELETE, INSERT и UPDATE, выбор правильного значения свойства **UpdateOptions** может значительно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-116">In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="3f2bd-117">Если не указать константы, будут использоваться **дбкритериаупдате** и **дбкритериакэй** .</span><span class="sxs-lookup"><span data-stu-id="3f2bd-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="3f2bd-118">Только что добавленные записи будут всегда создавать операторы INSERT и удаленные записи, которые всегда будут создавать операторы DELETE, поэтому это свойство применяется только к обновлению записей в библиотеке курсоров.</span><span class="sxs-lookup"><span data-stu-id="3f2bd-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

