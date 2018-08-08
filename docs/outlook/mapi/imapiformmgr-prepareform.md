---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3b10ac5906be0f95930be3bef51fe2d78d583b03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808949"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Относится к**: Outlook 
  
Файлы для загрузки для открытия формы.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения, который отображается при загрузке формы. Параметр _ulUIParam_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет способа загрузки формы. Можно задать следующий флаг:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления состояния или запрашивать у пользователя для получения дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
 _pfrmiInfo_
  
> [in] Указатель на объект сведения формы для формы веб-сайта.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Средства просмотра форм вызовите метод **IMAPIFormMgr::PrepareForm** можно загрузить из контейнера формы для открытия формы. Большинство средств просмотра формы не нужно вызвать **PrepareForm**, так как как [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) , так и [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) методы вызова **PrepareForm**, при необходимости. 
  
**PrepareForm** можно использовать для получения библиотеки динамической компоновки (DLL) и других файлов, связанный с формой для изменения их. Измененная форма загружается обратно в форму контейнера, необходимо повторно установить. 
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

