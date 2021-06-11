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
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416652"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Скачивает форму для открытия.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса, отображаемого во время загрузки формы. Параметр _ulUIParam_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют загрузку формы. Можно установить следующий флаг:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления статуса или запроса дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
 _pfrmiInfo_
  
> [in] Указатель на информационный объект формы для скачиваемой формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr::P repareForm,** чтобы скачать форму из контейнера формы для открытия. Большинству зрителей форм не нужно вызывать **PrepareForm,** так как оба [метода IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) и [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) называют **PrepareForm**, если это необходимо. 
  
Вы можете использовать **PrepareForm** для получения библиотек динамических ссылок (DLLs) и других файлов, связанных с формой для их изменения. Если измененная форма загружается обратно в контейнер формы, ее необходимо переустановить. 
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

