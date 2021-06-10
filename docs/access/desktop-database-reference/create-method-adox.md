---
title: Создание метода (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295424"
---
# <a name="create-method-adox"></a><span data-ttu-id="825cf-102">Создание метода (ADOX)</span><span class="sxs-lookup"><span data-stu-id="825cf-102">Create method (ADOX)</span></span>

<span data-ttu-id="825cf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="825cf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="825cf-104">Создает новый каталог.</span><span class="sxs-lookup"><span data-stu-id="825cf-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="825cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="825cf-105">Syntax</span></span>

<span data-ttu-id="825cf-106">*Каталог*. Создание *ConnectString*</span><span class="sxs-lookup"><span data-stu-id="825cf-106">*Catalog*.Create *ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="825cf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="825cf-107">Parameters</span></span>

|<span data-ttu-id="825cf-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="825cf-108">Parameter</span></span>|<span data-ttu-id="825cf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="825cf-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="825cf-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="825cf-110">*ConnectString*</span></span> |<span data-ttu-id="825cf-111">Значение **String,** используемое для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="825cf-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="825cf-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="825cf-112">Remarks</span></span>

<span data-ttu-id="825cf-113">Метод **Create** создает и открывает новое подключение [ADO](connection-object-ado.md) к источнику данных, указанному в *ConnectString.*</span><span class="sxs-lookup"><span data-stu-id="825cf-113">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*.</span></span> <span data-ttu-id="825cf-114">В случае успешной работы новый **объект Connection** назначен свойству [ActiveConnection.](activeconnection-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="825cf-114">If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="825cf-115">Ошибка возникает, если поставщик не поддерживает создание новых каталогов.</span><span class="sxs-lookup"><span data-stu-id="825cf-115">An error will occur if the provider does not support creating new catalogs.</span></span>

