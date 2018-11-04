---
title: Свойство URL-адрес (RDS - ссылки для настольных баз данных Access)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efba5d3703f41c54a03202dde2c3f30ffa17005a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949469"
---
# <a name="url-property-rds"></a><span data-ttu-id="48620-102">Свойство URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="48620-102">URL property (RDS)</span></span>

<span data-ttu-id="48620-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48620-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48620-104">Указывает строку, которая содержит относительный или абсолютный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="48620-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="48620-105">Можно задать свойство **URL-адреса** в тег OBJECT объекта [DataControl](datacontrol-object-rds.md) во время разработки или во время выполнения в код сценария.</span><span class="sxs-lookup"><span data-stu-id="48620-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="48620-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48620-106">Syntax</span></span>

<span data-ttu-id="48620-107">Время разработки: \<параметров имя = значение «URL-адрес» = «Сервер»\></span><span class="sxs-lookup"><span data-stu-id="48620-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="48620-108">Во время выполнения: DataControl.URL="Server»</span><span class="sxs-lookup"><span data-stu-id="48620-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="48620-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="48620-109">Parameters</span></span>

|<span data-ttu-id="48620-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="48620-110">Parameter</span></span>|<span data-ttu-id="48620-111">Описание</span><span class="sxs-lookup"><span data-stu-id="48620-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="48620-112">*Сервер*</span><span class="sxs-lookup"><span data-stu-id="48620-112">*Server*</span></span> |<span data-ttu-id="48620-113">**Строковое** значение, содержащее допустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="48620-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="48620-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="48620-114">*DataControl*</span></span> |<span data-ttu-id="48620-115">Объектная переменная, которая представляет собой объект- **DataControl** .</span><span class="sxs-lookup"><span data-stu-id="48620-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="48620-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="48620-116">Remarks</span></span>

<span data-ttu-id="48620-117">Как правило URL-адрес указывает файл страницы Active Server (.asp), который может создавать и возвращать [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="48620-117">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="48620-118">Таким образом пользователь может получить **записей** без вызова объекта [DataFactory](datafactory-object-rdsserver.md) на сервере или программа настраиваемый бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="48620-118">Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="48620-119">Если свойство **URL-адрес** [SubmitChanges](submitchanges-method-rds.md) будет внесения изменений в расположении, указанном URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="48620-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

