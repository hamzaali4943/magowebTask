<template>
  <q-page class="q-pa-lg">
    <div class="row shadow-2 border-radius-16 h-full">
      <div class="col-3 border-right scroll overflow-hidden">
        <div class="row justify-around  q-pl-lg q-pt-lg q-pb-md  border-bottom">
          <div class="column items-center text-primary">
            <q-icon name="style " size="md" class="text-h4" />
            <div class="text-caption">Chats</div>
          </div>
          <div class="column items-center">
            <q-icon name="font_download" class="text-secondary" size="md" />
            <div class="text-caption text-secondary">Groups</div>
          </div>
          <div class="column items-center text-secondary">
            <q-icon name="font_download" class="" size="md" />
            <div class="text-caption ">Terminal</div>
          </div>
          <q-separator vertical inset class="q-mb-sm" />
          <div class="q-mt-sm">
            <q-icon
              name="format_size"
              size="sm"
              class="shadow-3  q-mr-md q-pa-xs border-radius-20"
              style="color:#F7A834"
            />
            <q-icon
              name="format_size"
              size="sm"
              class="shadow-3 q-pa-xs border-radius-20"
              style="color:#F7A834"
            />
          </div>
        </div>
        <div class="q-mt-lg q-ml-lg items-center text-secondary row">
          <p class="text-caption">
            Recent Chats
          </p>
          <q-icon
            name="font_download"
            class="text-secondary q-ml-xs "
            size="xs"
          />
        </div>
        <q-scroll-area style="height: 550px; max-width: 800px;">
          <div v-for="index in 8" :key="index" class="overflow-y-auto">
            <div class="row justify-between q-pr-md">
              <div class="row items-center q-ml-lg">
                <div class="row">
                  <q-avatar size="lg">
                    <img src="https://cdn.quasar.dev/img/avatar.png" />
                  </q-avatar>
                  <div class="w-3 h-3 border-radius-full  bg-primary"></div>
                </div>
                <div class="q-ml-sm">
                  <div class="text-subtitle2  -q-mb-xs">John Doe</div>
                  <div class="text-caption text-secondary -q-mt-xs">
                    Account Manager
                  </div>
                </div>
              </div>
              <div class="text-right">
                <span
                  class="q-pa-xs bg-primary text-caption   border-radius-full pr-3 pl-3 text-white text-weight-medium "
                  >2</span
                >
                <div class="text-caption text-secondary q-pt-xs text-small-10">
                  3 mins ago
                </div>
              </div>
              <q-separator inset class="q-mt-md q-mb-lg" style="width:380px" />
            </div>
          </div>
        </q-scroll-area>
      </div>
      <div class="col-9 relative-position ">
        <div
          class="row justify-between items-center q-pt-lg border-bottom  pt-4 q-pb-lg"
        >
          <div class="row items-center q-ml-lg">
            <div class="row">
              <q-avatar size="lg">
                <img src="https://cdn.quasar.dev/img/avatar.png" />
              </q-avatar>
              <div class="w-3 h-3 border-radius-full  bg-primary"></div>
            </div>
            <div class="q-ml-sm">
              <div class="text-subtitle2">John Doe</div>
              <div class="text-caption text-secondary -q-mt-xs">
                Account Manager
              </div>
            </div>
          </div>
          <div>
            <q-icon
              name="format_size"
              size="sm"
              class="bg-positive q-mr-md q-pa-xs border-radius-20"
            />
            <q-icon
              name="format_size"
              size="sm"
              class=" bg-positive q-mr-md q-pa-xs border-radius-20"
            />
            <q-icon
              name="format_size"
              size="sm"
              class=" text-secondary q-mr-md q-pa-xs border-radius-20"
            />
          </div>
        </div>
        <div>
          <q-scroll-area style="height: 505px;">
            <div
              v-for="index in 2"
              :key="index"
              class="q-pa-md row justify-between"
            >
              <div style="width: 100%; ">
                <q-chat-message bg-color="positive" sent>
                  <div>
                    <div class="q-pa-sm q-pr-xl sent bg-positive q-pa-md">
                      <div class="text-weight-bold">
                        You
                      </div>
                      <div class="text-small">
                        hey, how are you?
                      </div>
                    </div>
                    <div class="text-right text-small text-secondary q-mr-md">
                      3pm
                    </div>
                  </div>
                </q-chat-message>
                <q-chat-message text-color="white">
                  <div>
                    <div class="q-pa-sm q-pr-xl received bg-primary q-pa-md">
                      <div class="text-small">
                        hey, how are you?
                      </div>
                    </div>
                    <div class="text-right text-small text-secondary q-mr-md">
                      3pm
                    </div>
                  </div>
                </q-chat-message>
              </div>
            </div>
            <div class="row items-center">
              <div class="col-1 border-dash q-ml-lg"></div>
              <div class="col-1 text-caption text-center">Today</div>
              <div class="col-9 border-dash"></div>
            </div>
            <div
              v-for="index in 6"
              :key="index"
              class="q-pa-md row justify-between"
            >
              <div style="width: 100%; ">
                <q-chat-message sent>
                  <div>
                    <div class="q-pa-sm q-pr-xl sent bg-positive q-pa-md">
                      <div class="text-weight-bold">
                        You
                      </div>
                      <div>
                        hey, how are you?
                      </div>
                    </div>
                    <div class="text-right text-caption text-secondary q-mr-md">
                      3pm
                    </div>
                  </div>
                </q-chat-message>
                <q-chat-message text-color="white">
                  <div>
                    <div class="q-pa-sm q-pr-xl received bg-primary  q-pa-md">
                      <div>
                        hey, how are you?
                      </div>
                    </div>
                    <div class="text-right text-caption text-secondary q-mr-md">
                      3pm
                    </div>
                  </div>
                </q-chat-message>
              </div>
            </div>
          </q-scroll-area>
        </div>
        <div
          class="absolute-bottom row items-center justify-around q-pb-lg q-pt-lg border-top"
        >
          <q-icon
            name="format_size"
            size="sm"
            class=" q-pa-xs  q-ml-md  text-secondary border-radius-20 "
          />
          <q-icon
            name="format_size"
            size="sm"
            class=" q-pa-xs q-ml-md text-secondary border-radius-20"
          />
          <div class="col-10 bg-info q-mr-md  border-radius-21">
            <div class="row items-center justify-around">
              <q-icon
                name="format_size"
                size="sm"
                class=" q-pa-sm text-secondary bg-white border-radius-20"
              />
              <q-input borderless class="col-10" />
              <q-icon
                name="format_size"
                size="sm"
                class=" bg-white text-primary q-pa-sm border-radius-20"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>
<style>
.sent {
  border-top-left-radius: 15px;
  border-bottom-left-radius: 15px;
  border-top-right-radius: 15px;
  border-bottom-right-radius: 0px;
}
.q-message-text--received {
  border-top-left-radius: 0px;
  border-bottom-left-radius: 15px;
  border-top-right-radius: 15px;
  border-bottom-right-radius: 15px;
  padding: 0%;
  background-color: transparent;
}
.received {
  border-top-left-radius: 0px;
  border-bottom-left-radius: 15px;
  border-top-right-radius: 15px;
  border-bottom-right-radius: 15px;
}
.q-message-text--sent {
  border-top-left-radius: 15px;
  border-bottom-left-radius: 15px;
  border-top-right-radius: 0px;
  border-bottom-right-radius: 15px;
  padding: 0%;
  background-color: transparent;
}
.q-message-text:last-child:before {
  display: none !important;
}
.height {
  height: 95vh;
  border-radius: 10px;
}
.line {
  height: 40px;
  width: 1px;
  background-color: black;
}
</style>
