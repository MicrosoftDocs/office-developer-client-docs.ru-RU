---
title: Свойство обработчика (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcb0b7f635e9ad74e6d8733a2f0fbe0153ac4739
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884872"
---
# <a name="handler-property-rds"></a><span data-ttu-id="04a07-102">Свойство обработчика (RDS)</span><span class="sxs-lookup"><span data-stu-id="04a07-102">Handler Property (RDS)</span></span>


<span data-ttu-id="04a07-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04a07-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="04a07-104">Указывает имя программы настройки на сервере (обработчик), которая расширяет возможности [RDSServer.DataFactory](datafactory-object-rdsserver.md)и все параметры, используемые в *обработчик*.</span><span class="sxs-lookup"><span data-stu-id="04a07-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04a07-105">Syntax</span></span>

<span data-ttu-id="04a07-106">*DataControl*. Обработчик = *строка*</span><span class="sxs-lookup"><span data-stu-id="04a07-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="04a07-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="04a07-107">Parameters</span></span>

  - <span data-ttu-id="04a07-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="04a07-108">*DataControl*</span></span>

  - <span data-ttu-id="04a07-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="04a07-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="04a07-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="04a07-110">*String*</span></span>

  - <span data-ttu-id="04a07-111">**Строковое** значение, содержащее имя обработчика и любых параметров, все запятыми (например, «handlerName, parm1, parm2,..., parm *N*»).</span><span class="sxs-lookup"><span data-stu-id="04a07-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="04a07-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="04a07-112">Remarks</span></span>

<span data-ttu-id="04a07-113">Это свойство поддерживает настройки, функциональные возможности, необходимо задать свойство [CursorLocation](cursorlocation-property-ado.md) **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="04a07-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="04a07-114">Имя обработчика и ее параметры при их наличии, разделенных запятыми («,»).</span><span class="sxs-lookup"><span data-stu-id="04a07-114">The name of the handler and its parameters, if any, are separated by commas (",").</span></span> <span data-ttu-id="04a07-115">Непредсказуемое поведение приведет к, если точку с запятой («;») в любом месте отображается в *строке*.</span><span class="sxs-lookup"><span data-stu-id="04a07-115">Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*.</span></span> <span data-ttu-id="04a07-116">Можно создать собственный обработчик условии, что он поддерживает интерфейс **IDataFactoryHandler** .</span><span class="sxs-lookup"><span data-stu-id="04a07-116">You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="04a07-117">Имя обработчика по умолчанию — **MSDFMAP. Обработчик**, и его параметр по умолчанию — это файл настройки с именем **MSDFMAP. INI**.</span><span class="sxs-lookup"><span data-stu-id="04a07-117">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**.</span></span> <span data-ttu-id="04a07-118">Это свойство используется для вызова настройки альтернативного файлы, созданные администратором сервера.</span><span class="sxs-lookup"><span data-stu-id="04a07-118">Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="04a07-119">Альтернатива для установки свойства **обработчика** — указание обработчика и параметры в свойство [ConnectionString](connectionstring-property-ado.md) ; то есть «\**обработчик = \*\*\* handlerName, parm1, parm2,...;*«.</span><span class="sxs-lookup"><span data-stu-id="04a07-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

