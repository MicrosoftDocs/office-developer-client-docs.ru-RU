---
title: Объект подключения (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95f70c233fdb299aa66c1cbeab9f5c27356c1e93
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026458"
---
# <a name="connection-object-dao"></a><span data-ttu-id="df921-102">Объект подключения (DAO)</span><span class="sxs-lookup"><span data-stu-id="df921-102">Connection object (DAO)</span></span>

<span data-ttu-id="df921-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df921-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="df921-104">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="df921-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="df921-105">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="df921-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="df921-106">Объект **подключения** представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="df921-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="df921-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="df921-107">Remarks</span></span>

<span data-ttu-id="df921-108">**Подключение** — это непостоянные объект, представляющий подключение к удаленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="df921-108">A **Connection** is a non-persistent object that represents a connection to a remote database.</span></span> <span data-ttu-id="df921-109">Объект **подключения** доступен только в рабочие области технология ODBCDirect (то есть, **рабочей области** объект, созданных с помощью параметра типа **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="df921-109">The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>

> [!NOTE]
> <span data-ttu-id="df921-110">Код, написанный для более ранних версий DAO можно продолжить использование объекта **базы данных** для обеспечения обратной совместимости, но при желании новые возможности **подключения** , необходимо проверить код, чтобы использовать объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="df921-110">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object.</span></span> <span data-ttu-id="df921-111">Чтобы упростить преобразование кода, можно получить ссылку на объект **подключения** из **базы данных** , прочитав статью свойство [Connection](database-connection-property-dao.md) объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="df921-111">To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object.</span></span> <span data-ttu-id="df921-112">С другой стороны можно получить ссылку на объект **базы данных** из свойства объекта **подключения к** **базе данных** .</span><span class="sxs-lookup"><span data-stu-id="df921-112">Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


