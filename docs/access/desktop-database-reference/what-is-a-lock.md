---
title: What is a Lock? (Справочник по базам данных Access на компьютере)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e503fd15d9864cc6ab007de031493e321622246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306764"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="88356-103">Что такое блокировка?</span><span class="sxs-lookup"><span data-stu-id="88356-103">What is a lock?</span></span>


<span data-ttu-id="88356-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88356-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88356-105">Блокировка — это процесс, с помощью которого СУБД запрещает доступ к строке в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="88356-105">Locking is the process by which a DBMS restricts access to a row in a multi-user environment.</span></span> <span data-ttu-id="88356-106">Если строка или столбец монопольно заблокированы, другие пользователи не могут получить доступ к заблокированным данным, пока не будет снята блокировка.</span><span class="sxs-lookup"><span data-stu-id="88356-106">When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released.</span></span> <span data-ttu-id="88356-107">Это гарантирует, что два пользователя не смогут одновременно обновить один столбец в строке.</span><span class="sxs-lookup"><span data-stu-id="88356-107">This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="88356-108">Блокировки могут быть очень дорогими с точки зрения ресурсов и использоваться только при необходимости сохранения целостности данных.</span><span class="sxs-lookup"><span data-stu-id="88356-108">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity.</span></span> <span data-ttu-id="88356-109">В базе данных, где сотни или тысячи пользователей могут пытаться получить доступ к записи каждую секунду (например, к базе данных, подключенной к Интернету), ненужная блокировка может быстро привести к снижению производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="88356-109">In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="88356-110">Вы можете управлять тем, как источник данных и библиотека курсоров ADO управляют параллелизмом, выбрав соответствующий параметр блокировки.</span><span class="sxs-lookup"><span data-stu-id="88356-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="88356-111">Задайте свойство **LockType** перед открытием объекта **Recordset** , чтобы указать тип блокировки, который должен использоваться поставщиком при его открытии.</span><span class="sxs-lookup"><span data-stu-id="88356-111">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it.</span></span> <span data-ttu-id="88356-112">Прочитайте свойство, чтобы возвратить тип блокировки, используемой в открытом объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="88356-112">Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="88356-113">Поставщики могут не поддерживать все типы блокировок.</span><span class="sxs-lookup"><span data-stu-id="88356-113">Providers might not support all lock types.</span></span> <span data-ttu-id="88356-114">Если поставщик не поддерживает запрошенный параметр **LockType** , он заменит другой тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="88356-114">If a provider cannot support the requested **LockType** setting, it will substitute another type of locking.</span></span> <span data-ttu-id="88356-115">Чтобы определить существующие функциональные возможности блокировки, доступные в объекте **Recordset** , используйте метод [](supports-method-ado.md) Supports с **адупдате** и **адупдатебатч**.</span><span class="sxs-lookup"><span data-stu-id="88356-115">To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="88356-116">Параметр **адлоккпессимистик** не поддерживается, если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="88356-116">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="88356-117">Если задано неподдерживаемое значение, ошибка не будет возникать; Вместо этого будет использоваться ближайшее поддерживаемое **LockType** .</span><span class="sxs-lookup"><span data-stu-id="88356-117">If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="88356-118">Свойство **LockType** доступно для чтения и записи, когда **набор записей** закрыт, и только для чтения при его открытии.</span><span class="sxs-lookup"><span data-stu-id="88356-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

<span data-ttu-id="88356-119">Этот раздел включает в себя следующие темы:</span><span class="sxs-lookup"><span data-stu-id="88356-119">This section includes the following topic:</span></span>

- [<span data-ttu-id="88356-120">Types of Locks</span><span class="sxs-lookup"><span data-stu-id="88356-120">Types of Locks</span></span>](types-of-locks.md)

