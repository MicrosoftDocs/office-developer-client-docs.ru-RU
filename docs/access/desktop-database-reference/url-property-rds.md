---
title: Свойство URL-адрес (RDS - ссылки для настольных баз данных Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f179eb2c251ca96943a5f924b0ca51881aa371b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874162"
---
# <a name="url-property-rds"></a><span data-ttu-id="4424c-102">Свойство URL-адрес (RDS)</span><span class="sxs-lookup"><span data-stu-id="4424c-102">URL Property (RDS)</span></span>


<span data-ttu-id="4424c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4424c-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="4424c-104">Указывает строку, которая содержит относительный или абсолютный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4424c-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="4424c-105">Можно задать свойство **URL-адреса** в тег OBJECT объекта [DataControl](datacontrol-object-rds.md) во время разработки или во время выполнения в код сценария.</span><span class="sxs-lookup"><span data-stu-id="4424c-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4424c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4424c-106">Syntax</span></span>

<span data-ttu-id="4424c-107">Время разработки: \<параметров имя = значение «URL-адрес» = «Сервер»\></span><span class="sxs-lookup"><span data-stu-id="4424c-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="4424c-108">Во время выполнения: DataControl.URL="Server»</span><span class="sxs-lookup"><span data-stu-id="4424c-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="4424c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4424c-109">Parameters</span></span>

  - <span data-ttu-id="4424c-110">*Сервер*</span><span class="sxs-lookup"><span data-stu-id="4424c-110">*Server*</span></span>

  - <span data-ttu-id="4424c-111">**Строковое** значение, содержащее допустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4424c-111">A **String** value that contains a valid URL.</span></span>

  - <span data-ttu-id="4424c-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="4424c-112">*DataControl*</span></span>

  - <span data-ttu-id="4424c-113">Объектная переменная, которая представляет собой объект- **DataControl** .</span><span class="sxs-lookup"><span data-stu-id="4424c-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4424c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4424c-114">Remarks</span></span>

<span data-ttu-id="4424c-115">Как правило URL-адрес указывает файл страницы Active Server (.asp), который может создавать и возвращать [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4424c-115">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="4424c-116">Таким образом пользователь может получить **записей** без вызова объекта [DataFactory](datafactory-object-rdsserver.md) на сервере или программа настраиваемый бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="4424c-116">Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="4424c-117">Если свойство **URL-адрес** [SubmitChanges](submitchanges-method-rds.md) будет внесения изменений в расположении, указанном URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4424c-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

