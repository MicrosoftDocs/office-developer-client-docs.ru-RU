---
title: Свойство MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289772"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="8bc00-102">Свойство MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="8bc00-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="8bc00-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bc00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bc00-104">Указывает, какие записи должны быть маршалией обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="8bc00-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8bc00-105">Параметры И значения возврата</span><span class="sxs-lookup"><span data-stu-id="8bc00-105">Settings And Return Values</span></span>

<span data-ttu-id="8bc00-106">Задает или возвращает [значение MarshalOptionsEnum.](marshaloptionsenum.md)</span><span class="sxs-lookup"><span data-stu-id="8bc00-106">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value.</span></span> <span data-ttu-id="8bc00-107">По умолчанию значение **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="8bc00-107">The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc00-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bc00-108">Remarks</span></span>

<span data-ttu-id="8bc00-109">При использовании клиентского пакета [записей](recordset-object-ado.md)записи, которые были изменены на клиенте, записывают обратно на средний уровень или веб-сервер с помощью метода маршализации, процесса упаковки и отправки параметров метода интерфейса через нитки или границы процесса.</span><span class="sxs-lookup"><span data-stu-id="8bc00-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="8bc00-110">Настройка свойства **MarshalOptions может** повысить производительность при сборе измененных удаленных данных для обновления на средний уровень или веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="8bc00-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="8bc00-111">**Удаленное использование службы данных** Это свойство используется только в клиентском **наборе Recordset.**</span><span class="sxs-lookup"><span data-stu-id="8bc00-111">**Remote Data Service Usage** This property is used only on a client-side **Recordset**.</span></span>

