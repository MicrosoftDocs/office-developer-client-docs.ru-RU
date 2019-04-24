---
title: Свойство Provider (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e640fb6131919cbdf88fbbf8229c62d0e2e4e13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301136"
---
# <a name="provider-property-ado"></a><span data-ttu-id="6ecfa-102">Свойство Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="6ecfa-102">Provider property (ADO)</span></span>


<span data-ttu-id="6ecfa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ecfa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ecfa-104">Указывает имя поставщика для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6ecfa-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6ecfa-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6ecfa-105">Settings and return values</span></span>

<span data-ttu-id="6ecfa-106">Задает или возвращает **строковое** значение, указывающее имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="6ecfa-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ecfa-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="6ecfa-107">Remarks</span></span>

<span data-ttu-id="6ecfa-108">Используйте свойство **provider** , чтобы задать или вернуть имя поставщика для подключения.</span><span class="sxs-lookup"><span data-stu-id="6ecfa-108">Use the **Provider** property to set or return the name of the provider for a connection.</span></span> <span data-ttu-id="6ecfa-109">Это свойство также можно задать с помощью содержимого свойства [ConnectionString](connectionstring-property-ado.md) или аргумента *ConnectionString* метода [Open](open-method-ado-connection.md) ; Однако при указании поставщика в нескольких местах при вызове метода **Open** могут возможно получить непредсказуемые результаты.</span><span class="sxs-lookup"><span data-stu-id="6ecfa-109">This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results.</span></span> <span data-ttu-id="6ecfa-110">Если поставщик не указан, свойство по умолчанию будет МСДАСКЛ ([Microsoft OLE DB Provider для ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="6ecfa-110">If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="6ecfa-111">Свойство **provider** доступно для чтения и записи, когда соединение закрывается и только для чтения при его открытии.</span><span class="sxs-lookup"><span data-stu-id="6ecfa-111">The **Provider** property is read/write when the connection is closed and read-only when it is open.</span></span> <span data-ttu-id="6ecfa-112">Параметр не вступает в силу до открытия объекта **Connection** или доступа к коллекции [свойств](properties-collection-ado.md) объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="6ecfa-112">The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="6ecfa-113">Если параметр не является допустимым, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="6ecfa-113">If the setting is not valid, an error occurs.</span></span>

