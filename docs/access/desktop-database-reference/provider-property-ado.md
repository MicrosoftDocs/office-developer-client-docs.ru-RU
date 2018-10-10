---
title: Provider Property (ADO)
TOCTitle: Provider Property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 890f80534ff47c4dea67b34f345bce0f90328c60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479745"
---
# <a name="provider-property-ado"></a><span data-ttu-id="e98b0-102">Provider Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e98b0-102">Provider Property (ADO)</span></span>


<span data-ttu-id="e98b0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e98b0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e98b0-104">Указывает имя поставщика для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e98b0-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e98b0-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e98b0-105">Settings and Return Values</span></span>

<span data-ttu-id="e98b0-106">Задает или возвращает **строковое** значение, указывающее имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="e98b0-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98b0-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="e98b0-107">Remarks</span></span>

<span data-ttu-id="e98b0-108">Используйте свойство **поставщика** или возвращает имя поставщика для подключения.</span><span class="sxs-lookup"><span data-stu-id="e98b0-108">Use the **Provider** property to set or return the name of the provider for a connection.</span></span> <span data-ttu-id="e98b0-109">Это свойство также можно установить с содержимое со значением свойства [ConnectionString](connectionstring-property-ado.md) или аргумент *ConnectionString* метода [Open](open-method-ado-connection.md) ; Тем не менее определение поставщика в нескольких местах, во время вызова метода **Open** может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="e98b0-109">This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results.</span></span> <span data-ttu-id="e98b0-110">Если поставщик не указан, свойство по умолчанию MSDASQL ([Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="e98b0-110">If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="e98b0-111">Свойство **поставщика** — чтение и запись при подключении закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="e98b0-111">The **Provider** property is read/write when the connection is closed and read-only when it is open.</span></span> <span data-ttu-id="e98b0-112">Параметр вступает в силу до при открытии объект **подключения** или коллекции [свойств](properties-collection-ado.md) объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="e98b0-112">The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="e98b0-113">Если параметр не является допустимым, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e98b0-113">If the setting is not valid, an error occurs.</span></span>

