---
title: DefaultDatabase Property (ADO)
TOCTitle: DefaultDatabase Property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 136e6bc0d68aac987a331ce20b8fca36a72afa73
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481776"
---
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="89dcc-102">DefaultDatabase Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="89dcc-102">DefaultDatabase Property (ADO)</span></span>


<span data-ttu-id="89dcc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89dcc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89dcc-104">Указывает базу данных по умолчанию для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="89dcc-104">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="89dcc-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="89dcc-105">Settings and Return Values</span></span>

<span data-ttu-id="89dcc-106">Задает или возвращает **строковое** значение, которое оценивается как имя базы данных, доступные из поставщика.</span><span class="sxs-lookup"><span data-stu-id="89dcc-106">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="89dcc-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="89dcc-107">Remarks</span></span>

<span data-ttu-id="89dcc-108">Свойство **DefaultDatabase** задает или возвращает имя базы данных по умолчанию для определенного объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="89dcc-108">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="89dcc-109">Если база данных по умолчанию, строк SQL использовать значение без указания единицы синтаксис для доступа к объектам в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="89dcc-109">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database.</span></span> <span data-ttu-id="89dcc-110">Для доступа к объектам в базу данных, указанных в свойстве **DefaultDatabase** , необходимо указать имена объектов с именем нужной базы данных.</span><span class="sxs-lookup"><span data-stu-id="89dcc-110">To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name.</span></span> <span data-ttu-id="89dcc-111">При подключении поставщика запишет сведения о базе данных по умолчанию для свойства **DefaultDatabase** .</span><span class="sxs-lookup"><span data-stu-id="89dcc-111">Upon connection, the provider will write default database information to the **DefaultDatabase** property.</span></span> <span data-ttu-id="89dcc-112">Некоторые поставщики разрешить подключения только одна база данных, в этом случае не может изменить свойство **DefaultDatabase** .</span><span class="sxs-lookup"><span data-stu-id="89dcc-112">Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="89dcc-113">Некоторые источники данных и поставщики могут не поддерживать этот компонент и может возвращать сообщение об ошибке или пустая строка.</span><span class="sxs-lookup"><span data-stu-id="89dcc-113">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="89dcc-114">**Службы удаленных данных об использовании** Это свойство недоступно на объект **подключения** со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="89dcc-114">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

