---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7170a28cb1d3ec9c8cdeca9229c255f264b9422e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883430"
---
# <a name="connection-object-dao"></a><span data-ttu-id="85eed-102">Connection Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="85eed-102">Connection Object (DAO)</span></span>


<span data-ttu-id="85eed-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85eed-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="85eed-104">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85eed-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85eed-105">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85eed-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



<span data-ttu-id="85eed-106">Объект **подключения** представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85eed-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="85eed-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="85eed-107">Remarks</span></span>

<span data-ttu-id="85eed-108">**Подключение** — это непостоянные объект, представляющий подключение к удаленной базе данных.</span><span class="sxs-lookup"><span data-stu-id="85eed-108">A **Connection** is a non-persistent object that represents a connection to a remote database.</span></span> <span data-ttu-id="85eed-109">Объект **подключения** доступен только в рабочие области технология ODBCDirect (то есть, **рабочей области** объект, созданных с помощью параметра типа **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="85eed-109">The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <span data-ttu-id="85eed-110">Код, написанный для более ранних версий DAO можно продолжить использование объекта **базы данных** для обеспечения обратной совместимости, но при желании новые возможности **подключения** , необходимо проверить код, чтобы использовать объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="85eed-110">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object.</span></span> <span data-ttu-id="85eed-111">Чтобы упростить преобразование кода, можно получить ссылку на объект **подключения** из **базы данных** , прочитав статью свойство [Connection](database-connection-property-dao.md) объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="85eed-111">To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object.</span></span> <span data-ttu-id="85eed-112">С другой стороны можно получить ссылку на объект **базы данных** из свойства объекта **подключения к** **базе данных** .</span><span class="sxs-lookup"><span data-stu-id="85eed-112">Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


