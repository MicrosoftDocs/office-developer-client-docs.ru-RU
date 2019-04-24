---
title: Компоненты и поставщики служб
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308703"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="21082-102">Компоненты и поставщики служб</span><span class="sxs-lookup"><span data-stu-id="21082-102">Service providers and components</span></span>


<span data-ttu-id="21082-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21082-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21082-104">Поставщики услуг — это компоненты, расширяющие функциональные возможности поставщиков данных за счет реализации расширенных интерфейсов, которые не поддерживаются в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="21082-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="21082-105">Microsoft Data Access предоставляет *архитектуру компонентов* , позволяющую отдельным специализированным компонентам реализовать дискретные наборы функций базы данных, или "службы", поверх менее производительных хранилищ.</span><span class="sxs-lookup"><span data-stu-id="21082-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="21082-106">Таким образом, вместо того чтобы принудительно использовать для каждого хранилища данных собственную реализацию расширенных функций или принудительно использовать универсальные приложения для внутренней реализации функциональности базы данных, компоненты службы предоставляют общую реализацию, которую может выполнять любое приложение. используется для доступа к любому хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="21082-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="21082-107">Тот факт, что некоторые функциональные возможности изначально реализованы в хранилище данных, а некоторые через универсальные компоненты прозрачны для приложения.</span><span class="sxs-lookup"><span data-stu-id="21082-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="21082-108">Например, обработчик курсора, например служба курсора (Майкрософт) для OLE DB, — это компонент службы, который может потреблять данные из последовательного и последующего прямого хранилища данных для создания прокручиваемых данных.</span><span class="sxs-lookup"><span data-stu-id="21082-108">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data.</span></span> <span data-ttu-id="21082-109">К другим поставщикам услуг, обычно используемым в ADO, относится поставщик сохраняемости Microsoft OLE DB (для сохранения данных в файл), Служба формирования данных (Майкрософт) для OLE DB (для иерархических **наборов записей**) и поставщик удаленного взаимодействия Microsoft OLE DB (для вызов поставщиков данных на удаленном компьютере).</span><span class="sxs-lookup"><span data-stu-id="21082-109">Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="21082-110">Дополнительные сведения о службах и поставщиках данных можно найти в [приложении а: поставщики](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="21082-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

