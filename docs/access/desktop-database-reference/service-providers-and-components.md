---
title: Компоненты и поставщики служб
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d215c7c66c489e54d513941604b1c66c0e9094c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881211"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="e502d-102">Компоненты и поставщики служб</span><span class="sxs-lookup"><span data-stu-id="e502d-102">Service Providers and Components</span></span>


<span data-ttu-id="e502d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e502d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e502d-104">Поставщики услуг — это компоненты, которые расширяют функциональные возможности поставщиков данных при помощи расширенные интерфейсы, которые изначально не поддерживаемых в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="e502d-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="e502d-105">*Архитектура компонентов* , которая позволяет отдельных, специализированных компонентов для реализации точечные задает функциональность базы данных или «службы» на менее производительные хранилищ предоставляет доступ к данным Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e502d-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="e502d-106">Таким образом а не на основе принудительным каждого хранилища данных для обеспечения собственная реализация расширенных функциональных возможностей или принудительную универсальных приложений для реализации функций базы данных во внутренней сети, компоненты службы обеспечивают общую реализацию, которая может в любое приложение Используйте при доступе к любому хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="e502d-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="e502d-107">Того факта, что некоторые функциональные возможности реализуется изначально хранилища данных и некоторые через общие компоненты прозрачен для приложения.</span><span class="sxs-lookup"><span data-stu-id="e502d-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="e502d-108">Например механизм курсора, таких как служба курсора для OLE DB — это компонент служб, который можно использовать данные из хранилища данных последовательные, однонаправленные для создания прокручиваемой данных.</span><span class="sxs-lookup"><span data-stu-id="e502d-108">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data.</span></span> <span data-ttu-id="e502d-109">Другие поставщики часто используемые ADO включают Microsoft поставщика OLE DB сохраняемость (для сохранения данных в файл), служба формирования данных Microsoft для OLE DB (для иерархические **наборы записей**) и поставщик Microsoft OLE DB удаленного взаимодействия (для вызов поставщики данных на удаленном компьютере).</span><span class="sxs-lookup"><span data-stu-id="e502d-109">Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="e502d-110">Дополнительные сведения о поставщиках службы и данные [В приложении A: поставщиков](appendix-a-providers.md)см.</span><span class="sxs-lookup"><span data-stu-id="e502d-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

