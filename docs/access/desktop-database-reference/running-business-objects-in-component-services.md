---
title: Выполнение бизнес-объектов в службах компонентов
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309208"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="81fc4-102">Выполнение бизнес-объектов в службах компонентов</span><span class="sxs-lookup"><span data-stu-id="81fc4-102">Running business objects in component services</span></span>

<span data-ttu-id="81fc4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81fc4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81fc4-104">Бизнес-объектами могут быть исполняемые файлы (EXE) или библиотеки динамической ссылки (DLL).</span><span class="sxs-lookup"><span data-stu-id="81fc4-104">Business objects can be executable files (.exe) or dynamic-link libraries (.dll).</span></span> <span data-ttu-id="81fc4-105">Конфигурация, используемая для запуска бизнес-объекта, зависит от того, является ли объект DLL-файлом или EXE-файлом:</span><span class="sxs-lookup"><span data-stu-id="81fc4-105">The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

- <span data-ttu-id="81fc4-106">Бизнес-объекты, созданные как EXE-файлы, могут быть вызваны с помощью DCOM.</span><span class="sxs-lookup"><span data-stu-id="81fc4-106">Business objects created as .exe files can be called through DCOM.</span></span> <span data-ttu-id="81fc4-107">Если эти бизнес-объекты используются через службы IIS, на них применяются дополнительные маршалинговые данные, что приводит к замедлению производительности клиента.</span><span class="sxs-lookup"><span data-stu-id="81fc4-107">If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

- <span data-ttu-id="81fc4-108">Бизнес-объекты, созданные в качестве DLL-файлов, можно использовать с помощью IIS (и, следовательно, HTTP).</span><span class="sxs-lookup"><span data-stu-id="81fc4-108">Business objects created as .dll files can be used via IIS (and therefore HTTP).</span></span> <span data-ttu-id="81fc4-109">Их также можно использовать через DCOM только через службы компонентов (или Microsoft Transaction Server, если вы используете Windows NT).</span><span class="sxs-lookup"><span data-stu-id="81fc4-109">They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT).</span></span> <span data-ttu-id="81fc4-110">DLL бизнес-объектов необходимо зарегистрировать на сервере IIS, чтобы предоставить вам доступ через IIS.</span><span class="sxs-lookup"><span data-stu-id="81fc4-110">Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS.</span></span> <span data-ttu-id="81fc4-111">(Действия по настройке DLL для запуска в DCOM см. в разделе["Включение DLL](enabling-a-dll-to-run-on-dcom.md)для запуска в DCOM.")</span><span class="sxs-lookup"><span data-stu-id="81fc4-111">(For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="81fc4-112">Когда бизнес-объекты на среднем уровне реализуются как компоненты служб компонентов (с помощью **GetObjectContext,** **SetComplete** и **SetAbort),** они могут использовать службы компонентов (или MTS, если вы используете Windows NT) для поддержания их состояния в нескольких клиентских вызовах.</span><span class="sxs-lookup"><span data-stu-id="81fc4-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="81fc4-113">Этот сценарий возможен с помощью DCOM, который обычно реализуется между доверенными клиентами и серверами (интрасеть).</span><span class="sxs-lookup"><span data-stu-id="81fc4-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="81fc4-114">В этом случае [RDS. Объект DataSpace](dataspace-object-rds.md) и метод [CreateObject](createobject-method-rds.md) на стороне клиента заменены объектом контекста транзакции и **методом CreateInstance** (предоставляемым интерфейсом **ITransactionContext),** реализованным службами компонентов.</span><span class="sxs-lookup"><span data-stu-id="81fc4-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="81fc4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="81fc4-115">See also</span></span>

- [<span data-ttu-id="81fc4-116">Запуск бизнес-объектов в службах компонентов (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="81fc4-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
