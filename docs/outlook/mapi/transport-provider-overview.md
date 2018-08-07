---
title: Обзор поставщиков транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812520"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="d2db3-103">Обзор поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="d2db3-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="d2db3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2db3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2db3-105">Поставщика транспорта — это библиотека динамической компоновки (DLL), которая выполняет роль посредника между подсистемы MAPI и один или несколько базовых систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d2db3-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="d2db3-106">Системы обмена сообщениями — некоторые определенные механизм, с помощью которого отправки и получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="d2db3-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="d2db3-107">Приведены некоторые примеры систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d2db3-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="d2db3-108">Файловая система общей сетевой, поставщика транспорта записывает сообщения, чтобы напрямую.</span><span class="sxs-lookup"><span data-stu-id="d2db3-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="d2db3-109">Сетевой интерфейс TCP/IP, поставщика транспорта для подключения к серверу обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d2db3-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="d2db3-110">Интерактивная служба, который пользователи подключаются к.</span><span class="sxs-lookup"><span data-stu-id="d2db3-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="d2db3-111">На основе узла обмена мгновенными сообщениями или office автоматизации система.</span><span class="sxs-lookup"><span data-stu-id="d2db3-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="d2db3-112">Набор удаленный вызов процедур в сервер обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d2db3-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="d2db3-113">Другие данные, которые можно использовать для передачи данных с одного компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="d2db3-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="d2db3-114">DLL-Библиотеки поставщика транспорта должен соответствовать типу интерфейса, указанная в MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2db3-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="d2db3-115">Разработчик, поставщика транспорта следует реализовать этот интерфейс с точки зрения функциональности в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d2db3-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

